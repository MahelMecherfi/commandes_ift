# 📦 Portail de Commandes de Matériel — IFT (Institut des Futures Technologies)

Projet WebTech A5 — Pôle Léonard de Vinci (DeVinci).

Application web responsive et sécurisée développée avec **Vue 3** et **Firebase (Firestore & Authentication)** pour la gestion, la validation et le suivi des demandes de matériel et composants pour les projets d'innovation et le FabLab de l'IFT.

---

## ✨ Fonctionnalités Principales

- **Authentification & Gestion des Rôles DeVinci :**
  - Accès restreint aux adresses du Pôle Léonard de Vinci (`@devinci.fr` et `@edu.devinci.fr`).
  - **Profil Étudiant / Demandeur (`@edu.devinci.fr`)** : Consultation des commandes, filtrage, soumission de nouvelles demandes de matériel.
  - **Profil Staff IFT / Administrateur (`@devinci.fr`)** : Droits complets d'édition, changement de statut, validation budgétaire et clôture des commandes.
  - Prévisualisation pour le Staff IFT permettant de basculer en vue Étudiant.
- **Cycle de Vie des Commandes :**
  - Progression des statuts : *En attente de revue (pendingIR)* → *Approuvée (approved)* → *Commandée (ordered)* → *Reçue (received)* → *Terminée (completed)* (ou *Refusée* / *Annulée*).
- **Interface & Expérience Utilisateur (Warm Editorial) :**
  - Design soigné sans débordement, typographies modernes (*Plus Jakarta Sans* & *Space Grotesk*).
  - Adaptation dynamique mobile & desktop (dézoom naturel et lisibilité optimale sur smartphone).
  - Recherche en temps réel, tri multi-critères (date, titre, montant, statut) et filtres par statut.
  - Statistiques en direct sur les volumes de commandes.
- **Sécurité & Backend Fiabilisé :**
  - Sanitization contre les injections XSS.
  - Contrôle strict des montants (positifs et plafonnés) et attribution vérifiée de l'identité du demandeur.
  - Règles de sécurité Firestore déployées ([firestore.rules](firestore.rules)).

---

## 🚀 Installation et Lancement Local

### Prérequis
- [Node.js](https://nodejs.org/) (version 18 ou supérieure recommandée)
- npm ou yarn

### 1. Cloner le dépôt
```bash
git clone https://github.com/MahelMecherfi/commandes_ift.git
cd commandes_ift
```

### 2. Installer les dépendances
```bash
npm install
```

### 3. Lancer le serveur de développement
```bash
npm run dev
```
L'application sera accessible sur [http://localhost:5173](http://localhost:5173).

### 4. Compiler pour la production
```bash
npm run build
```

---

## 🛠️ Stack Technique

- **Framework** : [Vue 3](https://vuejs.org/) (Composition API, `<script setup>`)
- **Build tool** : [Vite](https://vite.dev/)
- **Routage** : [Vue Router 4](https://router.vuejs.org/)
- **Backend / BDD** : [Google Firebase](https://firebase.google.com/) (Firestore & Firebase Auth)
- **Styles** : Vanilla CSS moderne avec design system basé sur des variables CSS, glassmorphism et animations subtiles.

---

## 👥 Auteur

- **Mahel Mecherfi** — Étudiant A5 Pôle Léonard de Vinci
