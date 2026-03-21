# Configurazione Google Drive Sync

## Procedura per ottenere il Client ID (una volta sola)

### 1. Vai su Google Cloud Console
https://console.cloud.google.com

### 2. Crea un nuovo progetto
- Clicca sul menu a tendina in alto → "New Project"
- Nome: `TAO Monitor`
- Clicca "Create"

### 3. Abilita Google Drive API
- Menu laterale → "APIs & Services" → "Library"
- Cerca "Google Drive API" → clicca → "Enable"

### 4. Configura la schermata OAuth
- Menu laterale → "APIs & Services" → "OAuth consent screen"
- User Type: **External** → "Create"
- App name: `TAO Monitor`
- User support email: la tua email
- Developer contact: la tua email
- Clicca "Save and Continue" per tutte le sezioni
- Nella sezione "Test users" → aggiungi le email che useranno l'app
- Clicca "Save and Continue"

### 5. Crea le credenziali OAuth
- Menu laterale → "APIs & Services" → "Credentials"
- "+ Create Credentials" → "OAuth client ID"
- Application type: **Web application**
- Name: `TAO Monitor Web`
- Authorized JavaScript origins → "+ Add URI":
  ```
  https://TUO-USERNAME.github.io
  ```
- Authorized redirect URIs → "+ Add URI":
  ```
  https://TUO-USERNAME.github.io/tao-monitor/
  ```
- Clicca "Create"

### 6. Copia il Client ID
- Vedrai una finestra con **Client ID** e Client Secret
- Copia il **Client ID** (formato: `xxxxx.apps.googleusercontent.com`)
- ⚠️ Non serve il Client Secret per questa app

### 7. Inserisci il Client ID nell'app
- Apri l'app → scheda "🛠 Strumenti" → sezione "Google Drive Sync"
- Incolla il Client ID → clicca "Connetti"

---

## Come funziona dopo la configurazione

1. **Prima apertura su ogni dispositivo**: clicca "Connetti Google Drive" → login Google
2. **Automatico**: l'app legge i dati da Drive all'apertura e scrive ad ogni modifica
3. **Conflitti**: se i dati su Drive sono più recenti di quelli locali, l'app chiede quale versione usare

## Privacy e sicurezza
- L'app accede SOLO al file `tao-data.json` che crea lei stessa
- Non vede altri file del tuo Google Drive
- Le credenziali OAuth non vengono mai salvate su server esterni
- Il token di accesso viene conservato nel browser e rinnovato automaticamente
