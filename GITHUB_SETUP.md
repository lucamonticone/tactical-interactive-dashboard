# GitHub setup — Tactical Interactive Dashboard

**Prima di iniziare:** il file della dashboard deve già esistere qui:

```text
C:\Users\lucam\Desktop\PROGETTI\TACTICAL_INTERACTIVE_DASHBOARD\Torino-Como26-27\tactical_view.html
```

Il pacchetto starter contiene SOLO i file da aggiungere alla cartella principale, non sostituisce la tua lavagna.

## 1. Estrai i file

Estrai il contenuto di questo ZIP **dentro** `TACTICAL_INTERACTIVE_DASHBOARD` (non creare una seconda cartella annidata). Al termine controlla:

```text
TACTICAL_INTERACTIVE_DASHBOARD/
├─ index.html
├─ README.md
├─ GITHUB_SETUP.md
├─ .nojekyll
├─ .gitignore
├─ assets/
│  └─ tactical-lab-icon.svg
└─ Torino-Como26-27/
   └─ tactical_view.html  ← il tuo file, già presente
```

**Nota Windows:** i file `.nojekyll` e `.gitignore` possono apparire nascosti in Esplora file, ma vengono aggiunti a Git normalmente.

## 2. Crea una repo vuota su GitHub

1. Vai su https://github.com/new
2. **Repository name:** `tactical-interactive-dashboard`
3. **Description:** `Interactive football tactical studies: build-up, pressing, passing lanes and defensive decisions.`
4. **Visibility:** `Public` (se vuoi GitHub Pages con GitHub Free)
5. **Non selezionare** `Add a README file`, `.gitignore` o `Choose a license`: sono già presenti localmente o si decideranno in seguito.
6. Premi **Create repository**.

## 3. Prima pubblicazione da PowerShell

Apri PowerShell e incolla, una riga alla volta:

```powershell
cd "C:\Users\lucam\Desktop\PROGETTI\TACTICAL_INTERACTIVE_DASHBOARD"
git --version
git init
git branch -M main
git status
git add .
git commit -m "Initial release: Tactical Lab and Torino-Como interactive case study"
git remote add origin https://github.com/TUO_USERNAME/tactical-interactive-dashboard.git
git push -u origin main
```

Sostituisci `TUO_USERNAME` con lo username esatto del tuo profilo GitHub. Se Git non conosce il tuo nome/email, configura prima:

```powershell
git config --global user.name "NOME CHE VUOI MOSTRARE"
git config --global user.email "EMAIL_ASSOCIATA_A_GITHUB"
```

Se `git remote add origin` dice che `origin` esiste già, esegui:

```powershell
git remote -v
git remote set-url origin https://github.com/TUO_USERNAME/tactical-interactive-dashboard.git
```

Per l'accesso GitHub, usa il login sicuro nel browser/Git Credential Manager se richiesto; non usare la password dell'account come password Git via HTTPS.

## 4. Attiva il sito pubblico

Apri la repository su GitHub:

`Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main → Folder: /(root) → Save`

Dopo che GitHub ha completato il deployment, avrai questi indirizzi:

```text
Homepage:
https://TUO_USERNAME.github.io/tactical-interactive-dashboard/

Dashboard Torino–Como:
https://TUO_USERNAME.github.io/tactical-interactive-dashboard/Torino-Como26-27/tactical_view.html
```

La versione finale del link va copiata da **Settings → Pages**, così non serve indovinare lo username.

## 5. Personalizza il README

Apri `README.md`, trova tutte le occorrenze di `TUO_USERNAME` e sostituiscile con il tuo vero username GitHub. Poi:

```powershell
git add README.md
git commit -m "Add live demo links to README"
git push
```

## 6. Aggiungere un nuovo caso studio

Crea una cartella nuova, ad esempio `TeamA-TeamB26-27`, e inserisci al suo interno il file HTML e tutti gli eventuali asset **relativi**. Aggiungi il link nel `index.html` della homepage e una riga nella tabella del `README.md`.

Per aggiornare il sito:

```powershell
cd "C:\Users\lucam\Desktop\PROGETTI\TACTICAL_INTERACTIVE_DASHBOARD"
git status
git add .
git commit -m "Add new interactive tactical case study"
git push
```

## Controlli prima di condividere su LinkedIn

- Apri la dashboard online in una scheda anonima: deve funzionare senza login.
- Testa play/pause, passaggi manuali e scenari anche da mobile/tablet se rilevante.
- Verifica che le risorse non puntino a `C:\...` o a `file:///...`.
- Se vengono usati `fetch()` o risorse esterne, verifica console Network e permessi CORS.
- Non pubblicare video coperti da copyright, dati interni del club, credenziali o dataset senza autorizzazione.
- Ricorda: **repo public = il sorgente HTML/JS è visibile a chiunque**. Se vuoi proteggere un algoritmo originale, non inserirlo in un HTML/JS pubblico.
- I nomi dei file nei link GitHub Pages sono **case-sensitive**: `Torino-Como26-27` e `tactical_view.html` devono corrispondere esattamente.

## Problemi comuni

**404 sul sito:** verifica che Pages pubblichi `main/(root)`, che `index.html` sia nella root e che il deployment in **Actions** sia terminato correttamente.

**Si vede la homepage ma non la dashboard:** controlla il nome esatto `Torino-Como26-27/tactical_view.html`, e che il file sia stato caricato nel commit.

**Layout diverso dall'ambiente locale:** controlla i path degli asset; usa percorsi relativi alla pagina (`./assets/...` o `../assets/...`) e non percorsi assoluti come `/assets/...` su una project page.

**`git` non riconosciuto:** installa Git for Windows da https://git-scm.com/downloads/win e riapri PowerShell.

---

Fonti per il flusso GitHub Pages: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
