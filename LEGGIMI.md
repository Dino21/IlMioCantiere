# Il Mio Cantiere

Tutta l'app è nel file **`index.html`** (grafica, logica e collegamento a Firebase).
Gli altri file servono solo per pubblicarla:

- `firebase.json` – cosa pubblicare
- `firestore.rules` – chi può leggere e scrivere i dati (amministratore / caposquadra)
- `.firebaserc` – il nome del progetto Firebase (`il-mio-cantiere`)

## Pubblicare dopo una modifica

Apri la cartella in Esplora file, scrivi `cmd` nella barra dell'indirizzo e premi Invio, poi:

```
firebase deploy
```

L'app è su **https://il-mio-cantiere.web.app**

## Provare in locale

Nella stessa finestra `cmd`: `firebase serve` e apri http://localhost:5000 (usa i dati veri).
