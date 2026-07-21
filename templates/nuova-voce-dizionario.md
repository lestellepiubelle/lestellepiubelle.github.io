<%*
const titolo = await tp.system.prompt("Titolo della voce");

if (!titolo) {
    new Notice("Creazione annullata");
    return;
}

// Crea lo slug per Hugo
const slug = titolo
    .toLowerCase()
    .normalize("NFD")
    .replace(/[\u0300-\u036f]/g, "")
    .replace(/[^a-z0-9\s-]/g, "")
    .trim()
    .replace(/\s+/g, "-");

// Percorso della nuova voce
const cartella = `content/dizionario/${slug}`;
const filePath = `${cartella}/index.md`;

// Controllo se esiste già
if (await app.vault.adapter.exists(filePath)) {
    new Notice("La voce esiste già: " + slug);
    return;
}

// Crea la cartella
await app.vault.createFolder(cartella);
await app.vault.createFolder(`${cartella}/immagini`);

// Data odierna
const oggi = tp.date.now("YYYY-MM-DD");

// Contenuto del file
const contenuto = `+++
title = "${titolo}"
date = "${oggi}"
draft = false
+++

{{< katex />}}

`;

// Crea index.md
const file = await app.vault.create(
    filePath,
    contenuto
);

// Apri il nuovo file
await app.workspace.getLeaf(false).openFile(file);
%>