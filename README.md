# Les 5 Concepts Clés du Développement by EKM Conseils

Un site pédagogique progressif et participatif pour maîtriser les fondamentaux du développement logiciel.

## 📚 Contenu du Cours

### Les 5 Concepts Essentiels

1. **Comprendre les API** (Application Programming Interface)
   - Structure d'une API REST
   - Création et consommation d'API

2. **Comprendre les différents rôles dans la technologie**
   - Développeur Backend, Frontend, Full-Stack
   - Data Scientist, DevOps, et autres métiers

3. **L'importance de se spécialiser**
   - Avantages de la spécialisation
   - Choisir sa voie

4. **Gérer efficacement son temps**
   - Technique Pomodoro
   - Importance des pauses

5. **Travailler en équipe et l'importance du réseau**
   - Utilisation de Git
   - Collaboration et mentorat

## 🎯 Fonctionnalités

- ✅ **Cours progressif** avec questions interactives
- 🛠️ **Activités pratiques** pour mettre en application
- 📝 **3 QCM d'évaluation** de 20 questions chacun
- 💾 **Sauvegarde automatique** des réponses
- 📊 **Suivi de progression** en temps réel
- 📧 **Export des résultats** par email ou PDF
- 🎨 **Design responsive** adapté à tous les écrans

## 🚀 Installation et Déploiement

### Prérequis

- Node.js (version 18 ou supérieure)
- npm ou yarn
- Git

### Installation locale

1. Cloner le repository :
```bash
git clone https://github.com/votre-username/5-concepts-dev.git
cd 5-concepts-dev
```

2. Installer les dépendances :
```bash
npm install
```

3. Lancer le serveur de développement :
```bash
npm run dev
```

4. Ouvrir le navigateur à l'adresse : `http://localhost:4321`

### Build pour la production

```bash
npm run build
```

Les fichiers de production seront générés dans le dossier `dist/`.

## 📦 Déploiement sur Netlify

### Option 1 : Déploiement automatique via GitHub

1. **Créer un repository GitHub** :
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/votre-username/5-concepts-dev.git
   git push -u origin main
   ```

2. **Connecter à Netlify** :
   - Aller sur [Netlify](https://app.netlify.com)
   - Cliquer sur "New site from Git"
   - Choisir GitHub et sélectionner votre repository
   - Configurer :
     - Build command: `npm run build`
     - Publish directory: `dist`
   - Cliquer sur "Deploy site"

3. **Configuration du domaine personnalisé** (optionnel) :
   - Dans les paramètres du site sur Netlify
   - Aller dans "Domain settings"
   - Ajouter votre domaine personnalisé

### Option 2 : Déploiement manuel

1. Builder le projet :
   ```bash
   npm run build
   ```

2. Installer Netlify CLI :
   ```bash
   npm install -g netlify-cli
   ```

3. Se connecter à Netlify :
   ```bash
   netlify login
   ```

4. Déployer :
   ```bash
   netlify deploy --prod
   ```

## 📱 Utilisation

### Pour les étudiants

1. **Identification** : Entrer nom, prénom, classe et date
2. **Cours** : Suivre les 5 concepts avec questions interactives
3. **Activités** : Compléter les 3 exercices pratiques
4. **QCM** : Valider les connaissances avec 3 niveaux
5. **Export** : Envoyer les résultats par email ou les imprimer

### Pour les formateurs

Le système sauvegarde automatiquement :
- Les informations des étudiants
- Les réponses aux questions du cours
- Les réponses aux activités pratiques
- Les résultats des QCM

## 🔧 Technologies Utilisées

- **Astro** - Framework de génération de sites statiques
- **HTML/CSS** - Structure et style
- **JavaScript** - Interactivité et logique
- **LocalStorage** - Sauvegarde des données
- **Netlify** - Hébergement et déploiement

## 📂 Structure du Projet

```
5-concepts-dev/
├── public/
│   └── images/
│       ├── logoekmconseilsv02.png
│       └── Diverse_Team_Unity_v02bis.png
├── src/
│   ├── layouts/
│   │   └── Layout.astro
│   └── pages/
│       ├── index.astro (Page d'accueil)
│       ├── identification.astro (Formulaire d'identification)
│       ├── cours.astro (Les 5 concepts)
│       ├── activites.astro (Activités pratiques)
│       └── qcm.astro (QCM d'évaluation)
├── astro.config.mjs
├── package.json
├── netlify.toml
└── README.md
```

## 🎨 Personnalisation

### Couleurs

Les couleurs sont définies dans le fichier `src/layouts/Layout.astro` :

```css
:root {
  --primary-color: #0066cc;
  --secondary-color: #00a8cc;
  --accent-color: #ff6b35;
  --text-color: #333;
  --bg-color: #f5f5f5;
}
```

### Images

Remplacer les images dans le dossier `public/images/` :
- `logoekmconseilsv02.png` : Logo de l'organisation
- `Diverse_Team_Unity_v02bis.png` : Image de fond de la page d'accueil

## 📧 Contact

Pour toute question ou suggestion :
- **Email** : contact@ekm-conseils.eu
- **Site web** : [www.ekmconseils.eu](https://www.ekmconseils.eu)

## 📝 Licence

© 2026 Eric MORMIN — Tous droits réservés  
Édité par EKM Conseils

---

**Auteur** : Eric MORMIN  
**Formateur** : BTS CIEL, BTS SIO  
**Organisation** : EKM Conseils - Expertise, Créativité, Solidarité
