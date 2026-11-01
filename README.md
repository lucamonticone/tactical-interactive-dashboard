# Tactical Interactive Dashboard

**Interactive football tactics, built to explore decisions rather than just describe them.**

> **Tactical Lab** è una raccolta di lavagne tattiche interattive dedicate a situazioni reali di calcio. Il progetto studia come il movimento di un giocatore possa cambiare le opzioni di passaggio, le coperture e le scelte dei compagni.

## Il progetto

L'idea nasce da un'osservazione semplice: guardando una partita dall'alto, il possesso non sembra una successione di passaggi isolati. Si vede la struttura collettiva: una squadra sposta la palla per muovere l'avversario e attende che si apra un accesso tra le linee.

Da qui nasce **Tactical Interactive Dashboard**: non una raccolta di screenshot, ma uno spazio in cui fermare il gioco, muovere la palla, confrontare le risposte difensive e osservare le conseguenze della stessa scelta tattica.

L'obiettivo è rendere **visibile il nesso tra struttura, comportamento e opportunità**, in un formato utilizzabile da analisti, allenatori e appassionati.

### Le domande a cui vogliamo rispondere

- Perché una squadra muove la palla orizzontalmente prima di verticalizzare?
- Come cambiano le linee disponibili quando un centrocampista esce, segue un uomo o protegge la zona?
- Cosa accade alle spalle della prima linea di pressione?
- Come si può mostrare un'alternativa difensiva partendo **dalla stessa situazione**?

## Interactive case studies

| # | Caso studio | Focus | Stato |
|---|---|---|---|
| 001 | **Torino – Como · 2026/27** | Costruzione del Como, 5-3-2 difensivo del Torino, ricerca degli spazi da parte di Nico Paz | Available |

**[Open the interactive Torino–Como tactical board](https://TUO_USERNAME.github.io/tactical-interactive-dashboard/Torino-Como26-27/tactical_view.html)**  
**[Visit the Tactical Lab homepage](https://TUO_USERNAME.github.io/tactical-interactive-dashboard/)**

> Sostituisci `TUO_USERNAME` con il tuo username GitHub prima del primo commit.

## Case study 001 — Torino × Como (2026/27)

Il primo caso studio è ambientato nel **primo tempo** di Torino–Como.

**Contesto tattico di partenza:**

- **Como:** 4-2-3-1, con Perrone da mediano. In alcune strutture di possesso un centrocampista può abbassarsi nella prima costruzione; questa è una **rotazione**, non un modulo di partenza a tre difensori.
- **Torino:** 5-3-2 come struttura difensiva di studio, con scivolamenti del centrocampo, uscite laterali e protezione del corridoio interno.
- **Focus:** Nico Paz cerca spazi tra centrocampo e difesa; Milla può offrire un appoggio o attirare un riferimento difensivo.

La lavagna permette di esplorare come lo stesso possesso possa offrire opportunità differenti in base alla decisione difensiva. Il cuore dell'analisi non è dichiarare che una squadra abbia certamente sbagliato: è **isolare una scelta e comprenderne il costo tattico**.

### Cosa puoi fare

1. Esplorare la disposizione dei 22 giocatori.
2. Seguire la circolazione del pallone e studiare le opzioni di passaggio.
3. Analizzare la differenza fra protezione di zona, marcatura e pressione.
4. Confrontare scenari didattici, osservando le conseguenze sui giocatori liberi e sulle linee interne.

Le interazioni esatte dipendono dalla versione della lavagna pubblicata in [`Torino-Como26-27/tactical_view.html`](Torino-Como26-27/tactical_view.html).

## Metodo e limiti

Questo progetto distingue esplicitamente tre livelli di evidenza:

| Livello | Significato |
|---|---|
| **Contesto reale** | Partita, squadre, impostazione tattica generale e osservazioni supportate da fonti. |
| **Modello geometrico** | Posizioni e linee rappresentate dalla lavagna, utili per esplorare possibilità nello scenario scelto. |
| **Simulazione didattica** | Movimenti e decisioni alternativi creati per spiegare un principio tattico; **non** equivalgono a tracking registrato della partita. |

**Importante:** una linea visivamente accessibile non rappresenta automaticamente un passaggio realizzabile con successo. Contano pressione, orientamento, velocità della palla, timing, tecnica e comportamenti degli altri giocatori. Le visualizzazioni non costituiscono una stima probabilistica validata, a meno che una singola analisi non lo dichiari e documenti esplicitamente.

Nessuna azione simulata va interpretata come prova che un determinato calciatore abbia effettivamente commesso un errore durante la partita.

### Riferimenti iniziali

- [Lega Serie A — Torino–Como: highlights](https://www.legaseriea.it/videos/serie-a-2026-2027-torino-como)
- Riferimenti video, formazioni e fonti specifiche saranno indicati nei singoli casi studio, quando disponibili e verificabili.

## Repository structure

```text
TACTICAL_INTERACTIVE_DASHBOARD/
├── README.md                      # Project history and methodology
├── index.html                     # Public Tactical Lab homepage
├── .nojekyll                      # Publish static assets as-is
├── .gitignore
├── assets/
│   └── tactical-lab-icon.svg
└── Torino-Como26-27/
    └── tactical_view.html         # Interactive case study 001
```

Ogni futura partita avrà una cartella dedicata, per esempio `TeamA-TeamB26-27/`. Un nuovo caso studio entra nella raccolta mantenendo lo stesso indirizzo dei precedenti.

## Run locally

Apri il file HTML direttamente nel browser. Se il progetto utilizza risorse esterne o richieste `fetch`, è preferibile avviare un semplice server statico dalla cartella principale:

```powershell
py -m http.server 8000
```

Poi apri `http://localhost:8000/`.

## Publishing

Il sito è pubblicato con **GitHub Pages** dalla branch `main`, cartella `/ (root)`. Ogni push pubblica la nuova versione dei file statici.

Per i passaggi completi di configurazione iniziale, vedi [`GITHUB_SETUP.md`](GITHUB_SETUP.md).

## Roadmap

- [x] Prima raccolta di un caso studio interattivo
- [ ] Validazione progressiva delle sequenze con video/tactical footage o tracking autorizzato
- [ ] Aggiunta di nuovi casi studio su costruzione, pressing e transizioni
- [ ] Documentazione tecnica specifica degli algoritmi per ogni progetto

## Transparency & rights

Progetto indipendente, non affiliato a Torino FC, Como 1907 o Lega Serie A. I nomi delle squadre sono utilizzati per descrivere un caso studio; il progetto non include per impostazione predefinita filmati di gara o loghi proprietari.

Il repository è pubblico per permettere di esplorare le demo. **Pubblicare un repository non equivale a concedere automaticamente una licenza di riutilizzo del codice.** Nessuna licenza open-source è stata selezionata per questo starter: deciderla esplicitamente se vuoi autorizzare il riuso.

---

<sub>Built for coaches, analysts and curious football minds. Observe the structure. Test the decision. Understand the space.</sub>
