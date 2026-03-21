# TAO Monitor — Installazione su GitHub Pages

## File necessari
```
index.html   ← app principale
manifest.json      ← configurazione PWA
sw.js              ← service worker (offline + notifiche)
icon-192.png       ← icona app (192x192)
icon-512.png       ← icona app (512x512)
```

## Procedura di installazione

### 1. Crea il repository GitHub
- Vai su [github.com](https://github.com) → **New repository**
- Nome: `tao-monitor` (o quello che preferisci)
- Visibilità: **Private** (consigliato per dati medici)
- Clicca **Create repository**

### 2. Carica i file
- Clicca **Add file** → **Upload files**
- Trascina tutti e 5 i file
- Clicca **Commit changes**

### 3. Attiva GitHub Pages
- Vai in **Settings** → **Pages**
- Source: **Deploy from a branch**
- Branch: **main** → cartella **/ (root)**
- Clicca **Save**

### 4. Aspetta ~2 minuti
- GitHub Pages sarà disponibile su:
  `https://TUO-USERNAME.github.io/tao-monitor/index.html`

### 5. Installa come app
**Android (Chrome):**
- Apri l'URL in Chrome
- Menu (⋮) → **Aggiungi a schermata Home**
- Conferma → l'app appare come icona nativa

**iPhone (Safari):**
- Apri l'URL in Safari
- Tocca il pulsante **Condividi** (□↑)
- Scorri e scegli **Aggiungi a schermata Home**

**Desktop Chrome:**
- Apri l'URL
- Clicca sull'icona 🖥 nella barra degli indirizzi
- Clicca **Installa**

## Aggiornamenti futuri
Quando aggiorni `index.html` su GitHub:
- Gli utenti che hanno l'app installata vedranno un banner
  "🔄 Nuova versione disponibile" con pulsante **Aggiorna**

## Privacy
- Repository **privato** = solo tu puoi vedere i file
- I dati del paziente rimangono nel browser (localStorage)
- Il backup JSON viene salvato nella cartella scelta dall'utente
- Nessun dato viene inviato a server esterni

## Prossimo step: Google Drive Sync
La prossima versione permetterà la sincronizzazione automatica
tra smartphone (paziente) e desktop (caregiver) tramite Google Drive.
