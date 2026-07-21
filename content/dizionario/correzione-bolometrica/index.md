+++
title = "Correzione bolometrica"
date = "2026-07-21"
draft = false
+++

{{< katex />}}

Come accennato nella voce Luminosità, nessun rilevatore è in grado di misurare il flusso totale di una stella, poiché l'atmosfera terrestre e gli stessi strumenti pongono dei limiti fisici. I telescopi campionano la luce attraverso filtri fotometrici (come il filtro $V$, centrato sul verde-giallo a circa 550 nanometri), che rappresentano solo una frazione delle lunghezze d'onda possibili.

## Definizione

Ma la radiazione emessa dalle stelle non è limitata a ciò che i nostri filtri fotometrici (le bande dello spettro) possono registrare. Ad esempio, una supergigante blu molto calda come Rigel irradia gran parte della sua energia nell'ultravioletto, mentre una nana rossa ultrafredda la disperde quasi interamente nell'infrarosso. La **correzione bolometrica**[^1] (indicata comunemente con la sigla $BC$, dall'inglese *Bolometric Correction*) è lo strumento teorico che gli astronomi usano per "recuperare" quella quota di radiazione *invisibile* ai filtri adoperati per misurare la radiazione stellare.

Tale correzione si basa sui modelli teorici di atmosfera stellare più aggiornati e consiste in un fattore numerico che varia a seconda del tipo di stella e che va a integrare le magnitudini stellari misurate, sia apparenti sia assolute, in modo da convertirle in magnitudini bolometriche.

Riferite alle magnitudini visuali apparenti e assolute, le formule fondamentali (nella convenzione standard adottata dall'Unione Astronomica Internazionale) sono:

$$
m_{bol} = m_V + BC_V \;\;\text{e}\;\; M_{bol} = M_V + BC_V
$$

## La correzione bolometrica è quasi sempre negativa

Dato che la magnitudine bolometrica rappresenta il flusso *totale* (che è sempre maggiore o uguale al flusso parziale misurato in una singola banda), e dato che nella scala delle magnitudini a un flusso maggiore corrisponde un valore numerico più piccolo, la correzione bolometrica è quasi sempre un valore *negativo* (o al massimo pari a zero). Se sommiamo alla magnitudine visibile un valore negativo, ne consegue che la magnitudine bolometrica è un numero più basso della magnitudine visibile, il che indica correttamente una maggiore brillantezza complessiva dell'astro osservato.

## I parametri che influiscono sulla correzione bolometrica

Il valore $BC$ varia da stella a stella, a volte drasticamente[^2], in funzione di tre parametri fondamentali: la **temperatura efficace** ($T_{\text{eff}}$), la **gravità superficiale** e la **metallicità** dell'astro. In base alla temperatura, possiamo osservare tre comportamenti tipici:

1. **Stelle caldissime (tipi spettrale O, B).** Poiché il loro picco di emissione è spostato decisamente verso l'ultravioletto, la luce visibile è solo una piccola frazione del totale. Di conseguenza, la loro $BC$ è fortemente negativa. Per le stelle di tipo O può superare il valore di $-3{,}0$ o $-4{,}0$.

2. **Stelle intermedie (tipi spettrale A, F, G).** Queste stelle, tra cui il Sole e Sirio, hanno il loro picco di emissione proprio all'interno o molto vicino alla banda visibile. La frazione di energia che sfugge al filtro è ridotta, quindi la loro $BC$ è molto vicina allo zero. Per il Sole $BC$ è approssimativamente pari a $-0{,}07$; per Sirio varia tra $-0{,}09$ e $-0{,}30$ a seconda delle calibrazioni.

3. **Stelle fredde (tipo spettrale M).** Avendo temperature superficiali basse, il loro picco si colloca nell'infrarosso. La luce visibile che emettono è pochissima rispetto all'energia termica totale irradiata. Di conseguenza, anche per le nane rosse o le supergiganti rosse il valore di $BC$ torna a essere marcatamente negativo.

## La correlazione tra tipo spettrale, temperatura e correzione bolometrica

La seguente tabella illustra in modo più dettagliato la relazione tra tipo spettrale, temperatura e correzione bolometrica.

| Tipo spettrale | Classe di luminosità | $T_{\text{eff}}$ (K) | $BC_V$ (mag) |
|---|---|---:|---:|
| O5 V | Nana | $\sim 42\,000$ | $\sim -4,0$ |
| B0 V | Nana | $\sim 30\,000$ | $\sim -3,0$ |
| A0 V | Nana | $\sim 9\,700$ | $\sim -0,5$ |
| F0 V | Nana | $\sim 7\,200$ | $\sim -0,1$ |
| G0 V | Nana | $\sim 6\,000$ | $\sim -0,07$ |
| G2 V | Nana (Sole) | $\sim 5\,778$ | $\sim -0,07$ |
| K0 V | Nana | $\sim 5\,200$ | $\sim -0,2$ |
| K5 V | Nana | $\sim 4\,400$ | $\sim -0,6$ |
| M0 V | Nana | $\sim 3\,800$ | $\sim -1,2$ |
| M5 V | Nana | $\sim 3\,200$ | $\sim -2,5$ |
| B0 I | Supergigante | $\sim 30\,000$ | $\sim -3,0$ |
| A0 I | Supergigante | $\sim 9\,700$ | $\sim -0,5$ |
| F0 I | Supergigante | $\sim 7\,700$ | $\sim -0,3$ |
| G0 I | Supergigante | $\sim 5\,700$ | $\sim -0,4$ |
| K0 I | Supergigante | $\sim 4\,500$ | $\sim -0,8$ |
| K5 I | Supergigante | $\sim 3\,800$ | $\sim -1,5$ |
| M0 I | Supergigante | $\sim 3\,700$ | $\sim -2,0$ |
| M2 I | Supergigante | $\sim 3\,600$ | $\sim -2,5$ |

[^1]: *Bolometrico* significa «relativo alla misura della radiazione totale». L'aggettivo deriva da *bolometro* (gr. *bolḗ*, «raggio di luce» più *métron*, «misura»), strumento ottocentesco ideato da Samuel Langley nel 1881 per misurare la potenza totale di una sorgente radiante.

[^2]: La determinazione della correzione bolometrica rimane una delle sfide più delicate della fotometria stellare. Poiché i flussi extra-visuali (soprattutto negli ultravioletti estremi per le stelle calde) sono difficili da calibrare anche con i telescopi spaziali, il valore esatto di $BC$ per una specifica classe spettrale può subire variazioni e aggiornamenti a seconda dei modelli teorici adottati dalle diverse équipe di ricerca.