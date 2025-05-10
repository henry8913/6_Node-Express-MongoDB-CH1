
# Blog Full-Stack

Un'applicazione web moderna per la gestione di un blog, realizzata con React per il frontend e Node.js/Express per il backend.

**Puoi vedere il sito live [Qui](https://6-node-express-mongo-db-ch-1-front-end.vercel.app/) 🌐**.

![Cover del progetto](img/cover.jpg)

## 📋 Descrizione

Questo blog full-stack offre una piattaforma completa per la pubblicazione e gestione di contenuti, con un'interfaccia utente reattiva e un backend robusto. Include un sistema di autenticazione sicuro per proteggere le funzionalità di pubblicazione e commento.

Per maggiori dettagli, puoi visitare i repository individuali:
- [Repository Frontend](https://github.com/henry8913/6_Node-Express-MongoDB-CH1_Front-end)
- [Repository Backend](https://github.com/henry8913/6_Node-Express-MongoDB-CH1_Back-end)

### ✨ Nuove Funzionalità
- Sistema di autenticazione con JWT e bcrypt
- Autenticazione OAuth 2.0 con Google
- Login e registrazione utenti (locale e Google)
- Protezione delle route sensibili
- Sistema di upload immagini con Cloudinary
- Editor di testo ricco con Draft.js
- Sistema di notifiche email per nuovi post
- Gestione avatar autori
- Sistema di categorizzazione avanzato
- Sistema di commenti interattivo con gestione CRUD
- Gestione personalizzata dei post (modifica/eliminazione) per gli autori
- Controllo di autorizzazione per operazioni sui post e commenti

## 🔄 Gestione del Monorepo

Il progetto utilizza una struttura monorepo con due script bash per semplificare la gestione:

### setup_monorepo.sh
Script per l'inizializzazione del monorepo che:
- Configura le repository remote per frontend e backend
- Importa il codice utilizzando git subtree
- Mantiene la cronologia dei commit

### push_subtrees.sh
Script per la sincronizzazione che:
- Aggiorna le repository individuali di frontend e backend
- Gestisce il push delle modifiche attraverso git subtree
- Mantiene sincronizzati tutti i repository

Per utilizzare gli script:
```bash
# Rendi gli script eseguibili
chmod +x setup_monorepo.sh
chmod +x push_subtrees.sh

# Setup iniziale
./setup_monorepo.sh

# Push delle modifiche
./push_subtrees.sh
```

## 🛠 Stack Tecnologico

### Frontend
- React 18
- React Bootstrap per UI components
- React Router DOM per la navigazione
- Draft.js per l'editor di testo
- React Icons

### Backend
- Node.js
- Express
- MongoDB con Mongoose
- Cloudinary per gestione immagini
- Sistema email con SendGrid
- CORS per la sicurezza
- Dotenv per la gestione delle variabili d'ambiente

## 🚀 Installazione e Avvio

### Prerequisiti
- Node.js
- MongoDB Atlas account
- Account Cloudinary
- Account SendGrid (per email)

### Configurazione

1. **Backend**:
```bash
cd Back-end
npm install
```

Crea un file `.env` con:
```
MONGODB_URL= # URL di connessione al database MongoDB
appName= # Nome dell'applicazione
PORT= # Porta su cui il server sarà in ascolto
FRONTEND_URL= #http://0.0.0.0:3000
BACKEND_URL= #http://0.0.0.0:8913

CLOUDINARY_CLOUD_NAME= # Nome del cloud su Cloudinary
CLOUDINARY_API_KEY= # Chiave API di Cloudinary
CLOUDINARY_API_SECRET= # Segreto API di Cloudinary

SENDGRID_API_KEY= # Chiave API di SendGrid per l'invio di email
ADMIN_EMAIL= # Email dell'amministratore
JWT_SECRET= # Chiave segreta per la generazione dei token JWT
SALT_ROUNDS= # Numero di round per la generazione dell'hash della password

GOOGLE_CLIENT_ID= # ID del client Google per OAuth 2.0
GOOGLE_CLIENT_SECRET= # Segreto del client Google per OAuth 2.0
```

2. **Frontend**:
```bash
cd Front-end
npm install
```

Crea un file `.env` con:
```
REACT_APP_API_URL= # URL del backend server
SENDGRID_API_KEY= # Chiave API di SendGrid
ADMIN_EMAIL= # Email per notifiche dei nuovi post
FRONTEND_URL= # URL del frontend
GOOGLE_CLIENT_ID= # ID del client Google per OAuth 2.0
GOOGLE_CLIENT_SECRET= # Segreto del client Google per OAuth 2.0
```

### Avvio dell'applicazione

1. **Backend**:
```bash
cd Back-end
npm run dev
```

2. **Frontend**:
```bash
cd Front-end
npm start
```

## 📝 API Endpoints

- `GET /posts` - Recupera tutti i post
- `GET /posts/:id` - Recupera un post specifico
- `POST /posts` - Crea un nuovo post
- `PUT /posts/:id` - Aggiorna un post
- `DELETE /posts/:id` - Elimina un post
- `GET /posts?title=:title` - Ricerca post per titolo
- `GET /authors/:authorName/posts` - Recupera i post di uno specifico autore
- `POST /posts/cover` - Upload immagine di copertina
- `POST /authors/avatar` - Upload avatar autore

### ✨ Caratteristiche Principali

#### 📝 Sistema di Gestione Articoli
- Visualizzazione di tutti i post nella homepage
- Creazione di nuovi post con editor di testo ricco
- Upload immagini integrate
- Modifica e eliminazione dei post esistenti
- Sistema di categorizzazione degli articoli

#### 🔍 Sistema di Ricerca Avanzato
- Ricerca dei post per titolo
- Filtro dei post per autore
- Risultati in tempo reale
- Interfaccia di ricerca intuitiva

#### 👥 Sistema Autori
- Profili autore personalizzati
- Avatar personalizzabili
- Visualizzazione di tutti i post di uno specifico autore
- Lista completa degli autori

#### 📱 Design e UX
- Interfaccia completamente responsive
- Design moderno e pulito
- Navigazione intuitiva
- Caricamento dinamico dei contenuti

#### 🛠 Funzionalità Tecniche
- API RESTful complete
- Integrazione MongoDB
- Upload immagini con Cloudinary
- Notifiche email automatiche
- Sistema di like per gli articoli
- Sistema di commenti per i post
- Gestione degli errori robusta
- Validazione dei dati

## 🤝 Contribuire

Le contribuzioni sono benvenute! Sentiti libero di:

- Forkare il repository
- Creare un branch per le tue modifiche
- Inviare una pull request

## 👤 Autore
Progetto creato da [Henry](https://github.com/henry8913) per scopi didattici.

## 📄 Licenza

Questo progetto è rilasciato sotto licenza MIT. Vedi il file LICENSE per i dettagli.
