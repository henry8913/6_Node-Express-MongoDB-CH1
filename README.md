
# Blog Full-Stack

Un'applicazione web moderna per la gestione di un blog, realizzata con React per il frontend e Node.js/Express per il backend.

**Puoi vedere il sito live [Qui](https://6-node-express-mongo-db-ch-1-front-end.vercel.app/) 🌐**.

![Cover del progetto](img/cover.jpg)

## 📋 Descrizione

Questo blog full-stack offre una piattaforma completa per la pubblicazione e gestione di contenuti, con un'interfaccia utente reattiva e un backend robusto.

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
- CORS per la sicurezza
- Dotenv per la gestione delle variabili d'ambiente

## 🚀 Installazione e Avvio

### Prerequisiti
- Node.js
- MongoDB Atlas account

### Configurazione

1. **Backend**:
```bash
cd Back-end
npm install
```

Crea un file `.env` con:
```
MONGODB_URL=il_tuo_url_mongodb
```

2. **Frontend**:
```bash
cd Front-end
npm install
```

Crea un file `.env` con:
```
REACT_APP_API_URL=http://localhost:8913
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

### ✨ Caratteristiche Principali

#### 📝 Sistema di Gestione Articoli
- Visualizzazione di tutti i post nella homepage
- Creazione di nuovi post con editor di testo ricco
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
- Sistema di like per gli articoli
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
