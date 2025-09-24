# Chat App – Projet Global

Ce projet regroupe une **application de chat en temps réel** composée de deux dépôts distincts :

* **Frontend** : Interface utilisateur en **React**, utilisant **TanStack Router**, **Zustand** et **Socket.IO client**.
* **Backend** : Serveur **NestJS** avec **Socket.IO** pour la communication WebSocket.

---

## Dépôts

* **Frontend** : [Lien vers le repo frontend](https://github.com/iDasrah/chat-app-client)
* **Backend**  : [Lien vers le repo backend](https://github.com/iDasrah/chat-app-server)

---

## Fonctionnalités principales

* **Connexion en temps réel** grâce à Socket.IO.
* **Authentification simple** : chaque utilisateur choisit un nom d'utilisateur, stocké localement.
* **Messages instantanés**.
* **Gestion d'état** côté client via **Zustand** pour l'authentification, le socket et les messages.
* **Séparation claire** du front et du back pour un déploiement indépendant.

---

## 🛠️ Stack Technique

| Partie    | Technologies clés                                                        |
| --------- | ------------------------------------------------------------------------ |
| **Front** | React, Vite, TanStack Router, Zustand, react-hook-form, Socket.IO client |
| **Back**  | NestJS, TypeScript, Socket.IO                                            |

---

## Lancer le projet localement

### 1️⃣ Backend

Suivre les instructions détaillées dans le [README du backend](https://github.com/iDasrah/chat-app-server).

### 2️⃣ Frontend

Suivre les instructions détaillées dans le [README du frontend](https://github.com/iDasrah/chat-app-client).

### 3️⃣ Variables d’environnement

Le frontend doit connaître l'URL du backend. Créez un fichier **.env** dans le dépôt front :

```env
VITE_SERVER_URL=http://localhost:3000
```

---

## Architecture globale

```
chat-app/
├─ client/    # Interface utilisateur React + TanStack Router
└─ server/    # API NestJS + Socket.IO
```

> 💡 **Conseil déploiement** : tu peux déployer le backend (NestJS) sur une plateforme comme Railway/Render/Heroku et le frontend (Vite/React) sur Vercel ou Netlify. Assure-toi simplement de mettre à jour `VITE_SERVER_URL` avec l'URL publique du backend.
