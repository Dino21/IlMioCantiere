# Il Mio Cantiere

Tutta l'app è nel file **`index.html`** (grafica, logica e collegamento a Firebase).
Gli altri file servono solo per pubblicarla:

- `firebase.json` – cosa pubblicare
- `firestore.rules` – chi può leggere e scrivere i dati (amministratore / caposquadra)
- `.firebaserc` – il nome del progetto Firebase (`il-mio-cantiere`)
- `deploy.bat` e `.github/workflows/deploy.yml` – pubblicazione a mano e automatica

## Pubblicare dopo una modifica

Prima di pubblicare aggiorna `APP_VER` in cima allo script di `index.html` (data `AAAA.MM.GG`, più una lettera se è la
seconda modifica del giorno: `2026.11.15b`). La versione si vede nella Panoramica e chi ha l'app aperta vede la barra
"È disponibile una nuova versione".

- **In automatico**: basta fare push su `main` con `index.html` (o `firebase.json`) cambiato. GitHub pubblica da solo
  (`.github/workflows/deploy.yml`, scheda *Actions* del repository; da lì si può anche avviare a mano con *Run workflow*).
  Pubblica solo l'app: se cambi `firestore.rules` usa `deploy.bat`.
- **A mano**: doppio clic su **`deploy.bat`** (pubblica app e regole di Firestore; equivale a `firebase deploy`).

L'app è su **https://il-mio-cantiere.web.app**

## Provare in locale

Apri la cartella in Esplora file, scrivi `cmd` nella barra dell'indirizzo e premi Invio, poi `firebase serve` e apri http://localhost:5000 (usa i dati veri).
