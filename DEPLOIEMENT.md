# Guide de Déploiement Rapide
# Les 5 Concepts Clés du Développement by EKM Conseils

## ⚡ Déploiement Rapide sur Netlify (5 minutes)

### Étape 1 : Préparer le projet

1. Ouvrez un terminal dans le dossier du projet
2. Initialisez Git (si pas encore fait) :
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Les 5 Concepts Clés du Développement"
   ```

### Étape 2 : Créer un repository GitHub

1. Allez sur [GitHub](https://github.com)
2. Créez un nouveau repository nommé `5-concepts-dev-ekm`
3. Dans votre terminal, liez votre projet :
   ```bash
   git remote add origin https://github.com/VOTRE-USERNAME/5-concepts-dev-ekm.git
   git branch -M main
   git push -u origin main
   ```

### Étape 3 : Déployer sur Netlify

#### Option A : Via l'interface Netlify (Recommandé)

1. Allez sur [Netlify](https://app.netlify.com)
2. Cliquez sur "New site from Git"
3. Choisissez "GitHub" et autorisez l'accès
4. Sélectionnez votre repository `5-concepts-dev-ekm`
5. Configurez :
   - **Build command**: `npm run build`
   - **Publish directory**: `dist`
6. Cliquez sur "Deploy site"
7. Attendez 2-3 minutes (le site sera disponible)

#### Option B : Via Netlify CLI

1. Installez Netlify CLI :
   ```bash
   npm install -g netlify-cli
   ```

2. Connectez-vous :
   ```bash
   netlify login
   ```

3. Déployez :
   ```bash
   netlify deploy --prod
   ```

### Étape 4 : Personnaliser le domaine (Optionnel)

1. Dans Netlify, allez dans les paramètres du site
2. Cliquez sur "Domain settings"
3. Ajoutez votre domaine personnalisé
4. Suivez les instructions pour configurer les DNS

## 🔧 Configuration Netlify (netlify.toml)

Le fichier `netlify.toml` est déjà configuré avec :

```toml
[build]
  command = "npm run build"
  publish = "dist"

[[redirects]]
  from = "/*"
  to = "/index.html"
  status = 200
```

## 📝 Checklist Avant Déploiement

- [ ] Les images sont présentes dans `public/images/`
- [ ] Le fichier `package.json` est à jour
- [ ] Le fichier `netlify.toml` est présent
- [ ] Git est initialisé et le code est commité
- [ ] Le repository GitHub est créé et lié

## 🎯 URLs Importantes

Une fois déployé, vous aurez :
- **URL Netlify** : `https://nom-du-site.netlify.app`
- **URL personnalisée** : `https://votre-domaine.com` (si configuré)

## 📧 Support

Pour toute aide :
- Documentation Astro : https://docs.astro.build
- Documentation Netlify : https://docs.netlify.com
- Contact EKM Conseils : contact@ekm-conseils.eu

## ⚠️ Notes Importantes

1. **Premier déploiement** : Peut prendre 5-10 minutes
2. **Builds automatiques** : Chaque push sur GitHub redéploie le site
3. **Prévisualisation** : Les Pull Requests créent des previews automatiques
4. **Sauvegarde des données** : Les données sont stockées en localStorage (navigateur de l'utilisateur)

## 🚀 Après le Déploiement

### Partager avec les étudiants

1. Copiez l'URL Netlify
2. Partagez-la sur EcoleDirecte ou par email
3. Les étudiants peuvent immédiatement commencer à utiliser la plateforme

### Mettre à jour le site

```bash
# Modifier les fichiers
git add .
git commit -m "Description des modifications"
git push

# Netlify redéploiera automatiquement
```

### Surveiller l'utilisation

- Allez dans le dashboard Netlify
- Consultez les statistiques de visite
- Vérifiez les logs de build en cas de problème

## 💡 Astuces

1. **Tester localement avant de déployer** :
   ```bash
   npm run build
   npm run preview
   ```

2. **Variables d'environnement** :
   - Configurez-les dans Netlify UI
   - Onglet "Environment variables"

3. **Déploiements multiples** :
   - Créez des branches pour différentes versions
   - Chaque branche peut avoir sa propre preview URL

---

**Auteur** : Eric MORMIN  
**Organisation** : EKM Conseils  
**Date** : Janvier 2026
