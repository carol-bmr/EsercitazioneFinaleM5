# Report Power BI — Olist Store (Brazilian E-Commerce)

Report di Business Intelligence sul dataset pubblico **Olist**, sviluppato come
esercitazione di fine modulo (EFM_M5) del corso Data Analyst di Epicode.

**Autrice:** Carol Pagano
**Strumento:** Microsoft Power BI Desktop
**Dataset:** Olist Store — ordini di vendita 2016–2018 (pubblico e anonimizzato)

---

## Cos'è

Un report interattivo che analizza le performance del marketplace brasiliano Olist su tre assi:

- **Andamento degli ordini** nel tempo, per stato dell'ordine e area geografica
- **Andamento dei ricavi** nel tempo, con confronto anno-su-anno e variazioni mensili
- **Distribuzione del rating** e soddisfazione dei clienti

Il modello è costruito come **star schema** con dimensione calendario dedicata, e il report
è pensato per essere chiaro e leggibile anche a chi non è esperto di dati.

## Numeri chiave (dataset 2016–2018)

| Metrica | Valore |
|---|---|
| Articoli venduti | ~113.000 |
| Ricavi totali | R$ 15,85 Mln |
| Recensioni | 99.224 |
| Rating medio | 4,09 / 5 |
| Periodo | 04/09/2016 → 17/10/2018 |

## Come aprire il report

1. Installa **Power BI Desktop** (versione recente, gratuita da Microsoft Store).
2. Apri il file `Esercitazione.pbix`.
3. I dati sono già incorporati nel modello: il report è pronto all'uso, non serve ricaricare i CSV.
4. Parti dalla pagina **Presentazione** e clicca **"Entra nel report"**.

> Per una semplice consultazione senza installare nulla, apri `Esercitazione.pdf`
> (esportazione visiva completa del report).

## Il dataset

Il report usa il **Brazilian E-Commerce Public Dataset by Olist**, pubblico e anonimizzato.
I file CSV originali **non sono inclusi in questa repository** (pesano oltre 100 MB) e sono
già incorporati nel file `.pbix`. Per scaricarli separatamente:

**https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce**

Le tabelle usate nel report sono: orders, order_items, products, order_reviews, customers
(più la tabella di traduzione delle categorie).

## Struttura del report (10 pagine)

| # | Pagina | Contenuto |
|---|--------|-----------|
| — | Presentazione | Copertina con KPI globali e accesso al report |
| 1 | Overview | Sintesi: KPI, ordini per mese, top stati e categorie |
| 2 | Ordini | Andamento mensile ordini, consegne, top stati |
| 3 | Ricavi | Ricavi mensili vs anno precedente, top stati, ricavi per categoria |
| 4 | Rating | Distribuzione voti, recensioni autentiche, rating per categoria |
| — | Dettaglio Categoria | Drill-through: focus su una singola categoria |
| — | Dettaglio Stato | Drill-through: focus su un singolo stato |
| — | TT Ordini / TT Ricavi | Tooltip con la variazione % mese/mese |
| — | Info & Metodologia | Glossario delle misure e scelte metodologiche |

## Funzionalità principali

- **Slicer Anno** sincronizzato tra le pagine principali
- **Semaforo colori** sullo slicer Stato Ordini (🟢 dati completi · 🟠 parziali · 🔴 minimi/assenti)
- **Note dinamiche** che cambiano in base ad anno e stato selezionati
- **Drill-through** su categoria e stato
- **Tooltip** con variazione % mese/mese
- **Recensioni autentiche** dei clienti (in portoghese), mostrate senza modifiche

## File inclusi

- `Esercitazione.pbix` — il report Power BI (dati incorporati)
- `Esercitazione.pdf` — esportazione visiva del report, consultabile senza Power BI
- `Misure_DAX_Olist.xlsx` — catalogo di tutte le misure DAX del modello
- `Documento_Metodologico.docx` — le scelte metodologiche e il perché
- `Traccia_Esercitazione.docx` — la traccia originale dell'esercitazione

> I CSV del dataset **non** sono inclusi (vedi sezione *Il dataset*).

## Principio guida

**Nessun dato è stato cancellato, tagliato o inventato.** Dove serviva leggibilità
(nomi di categorie, città, stati) sono state aggiunte colonne derivate accanto alle
originali, mai sostituite. I valori che possono sembrare anomali (2016 parziale, 2018
troncato ad agosto) sono reali e spiegati nel report.

---

*Dataset: Olist Store — pubblico e anonimizzato. Progetto a scopo didattico.*
