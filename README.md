# Mobilità sanitaria – dataviz Radar QN

| Dataviz | URL | Dati |
|---|---|---|
| Oncologia: quota di ricoveri fuori regione nel Mezzogiorno (barre) e destinazioni per regione (Sankey a ventaglio), 2024 | https://cosimofire.github.io/mobilita-sanitaria/oncologia/ | `data/oncologia-flussi.csv` |
| Muscolo-scheletrico: stessa struttura, 2024 | https://cosimofire.github.io/mobilita-sanitaria/muscolo-scheletrico/ | `data/muscolo-scheletrico-flussi.csv` |

**Fonte:** Svimez, Rapporto 2026, cap. 16, Tab. 3 (area oncologica) e Tab. 5 (area muscolo-scheletrica), su dati Agenas.

**Dati:** matrice completa provenienza × destinazione (21 regioni e province autonome, separatore `;`), diagonale compresa. La pagina usa solo i ricoveri fuori dalla regione di residenza e ricava dalla diagonale le quote nei popup. Trascrizione verificata: per ogni riga e colonna le somme coincidono con i totali delle tabelle Svimez; le somme di colonna senza diagonale coincidono con l'attrazione Agenas. I flussi tra singole regioni sono ricostruiti da Svimez (vedi nota (a) delle tabelle): sono stime. La somma di riga senza diagonale può differire di pochi ricoveri dalla fuga Agenas.

**Struttura della pagina:** in alto barre orizzontali con la quota di ricoveri dei residenti fatti fuori regione, per le 8 regioni del Mezzogiorno e per il Mezzogiorno nel suo insieme, divise tra destinazioni al Centro-Nord e in altre regioni del Sud; linea tratteggiata = media delle regioni del Centro-Nord. Sotto, Sankey a ventaglio "Dove vanno a curarsi": una regione di partenza (menu con tutte le 21 regioni, oppure tocco su una barra) verso sette destinazioni fisse (le cinque del Centro-Nord che ricevono più pazienti dal Mezzogiorno, altre regioni del Centro-Nord, altre regioni del Sud) in ordine decrescente. Sotto il nome della regione: posizione su 21 per quota di ricoveri fuori regione. Tutto è calcolato nel browser dal CSV.

**File:** il codice è dentro le due `index.html`; `radar.css`, `radar.js`, `embed*.js` e `logo/` vengono dalla skill radar-dataviz (copiati da `caffe`). Librerie: d3 v7 e d3-sankey 0.12.3 da jsDelivr.

## Sfondo e logo

Come nelle altre dataviz Radar: la pagina riconosce i quattro sfondi QN. Anteprime: `?bg=grigio`, `?bg=bianco`, `?bg=nero`, `?bg=notte`.

## Snippet per il CMS

Sono nella pagina indice (https://cosimofire.github.io/mobilita-sanitaria/), con il pulsante Copia.
