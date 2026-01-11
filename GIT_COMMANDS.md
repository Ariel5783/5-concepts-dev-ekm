# Commandes Git Essentielles
# Pour le projet "Les 5 Concepts Clés du Développement"

## 🎯 Configuration Initiale

### Configurer votre identité Git (une seule fois)
```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
```

### Vérifier votre configuration
```bash
git config --list
```

## 🚀 Initialisation du Projet

### Initialiser un dépôt Git dans le projet
```bash
cd 5-concepts-dev
git init
```

### Ajouter tous les fichiers
```bash
git add .
```

### Premier commit
```bash
git commit -m "Initial commit: Les 5 Concepts Clés du Développement"
```

## 🔗 Connexion avec GitHub

### Créer la connexion avec un repository distant
```bash
git remote add origin https://github.com/VOTRE-USERNAME/5-concepts-dev-ekm.git
```

### Renommer la branche principale en "main"
```bash
git branch -M main
```

### Pousser le code vers GitHub
```bash
git push -u origin main
```

## 📝 Workflow Quotidien

### 1. Vérifier le statut des fichiers
```bash
git status
```

### 2. Ajouter des fichiers modifiés
```bash
# Ajouter un fichier spécifique
git add nom-du-fichier.ext

# Ajouter tous les fichiers modifiés
git add .

# Ajouter tous les fichiers d'un dossier
git add src/
```

### 3. Faire un commit
```bash
git commit -m "Description claire des modifications"
```

**Exemples de bons messages de commit :**
- `git commit -m "Ajout: Nouvelle question dans le QCM niveau 1"`
- `git commit -m "Fix: Correction du calcul de score dans le QCM"`
- `git commit -m "Amélioration: Design responsive des cartes de concepts"`
- `git commit -m "Documentation: Mise à jour du README"`

### 4. Pousser vers GitHub
```bash
git push
```

## 🔄 Récupérer les Modifications

### Récupérer les dernières modifications depuis GitHub
```bash
git pull
```

## 📊 Historique et Information

### Voir l'historique des commits
```bash
git log

# Version compacte
git log --oneline

# Avec graphique
git log --oneline --graph --all
```

### Voir les modifications d'un fichier
```bash
git diff nom-du-fichier.ext

# Voir toutes les modifications non commitées
git diff
```

## 🌿 Branches

### Créer une nouvelle branche
```bash
git branch nom-de-la-branche
```

### Changer de branche
```bash
git checkout nom-de-la-branche
```

### Créer et changer de branche en une commande
```bash
git checkout -b nom-de-la-branche
```

### Lister toutes les branches
```bash
git branch
```

### Fusionner une branche dans la branche actuelle
```bash
git merge nom-de-la-branche
```

### Supprimer une branche locale
```bash
git branch -d nom-de-la-branche
```

## 🔙 Annuler des Modifications

### Annuler les modifications d'un fichier non commité
```bash
git checkout -- nom-du-fichier.ext
```

### Annuler tous les fichiers modifiés non commités
```bash
git checkout -- .
```

### Retirer un fichier de l'index (avant commit)
```bash
git reset HEAD nom-du-fichier.ext
```

### Annuler le dernier commit (en gardant les modifications)
```bash
git reset --soft HEAD~1
```

### Annuler le dernier commit (en supprimant les modifications)
```bash
git reset --hard HEAD~1
```

## 🔍 Commandes Utiles

### Voir les fichiers ignorés
```bash
git status --ignored
```

### Supprimer les fichiers non suivis
```bash
git clean -n  # Voir quels fichiers seront supprimés
git clean -f  # Supprimer effectivement
```

### Cloner un repository existant
```bash
git clone https://github.com/username/repository.git
```

## 📁 Fichier .gitignore

Le fichier `.gitignore` est déjà configuré pour ignorer :
- `node_modules/` - Dépendances npm
- `dist/` - Fichiers de build
- `.env` - Variables d'environnement
- `.DS_Store` - Fichiers macOS
- `*.log` - Fichiers de logs

## 🆘 Résolution de Problèmes

### Problème : "fatal: not a git repository"
```bash
# Vous n'êtes pas dans un dépôt Git
git init  # Initialisez-en un
```

### Problème : Conflit lors d'un merge
```bash
# 1. Ouvrez les fichiers en conflit
# 2. Résolvez les conflits manuellement
# 3. Ajoutez les fichiers résolus
git add .
git commit -m "Résolution des conflits"
```

### Problème : "Permission denied" lors du push
```bash
# Configurez votre authentification SSH ou utilisez HTTPS
git remote set-url origin https://github.com/username/repo.git
```

## 📚 Workflow Recommandé pour ce Projet

### 1. Développement Local
```bash
# Créer une branche pour une nouvelle fonctionnalité
git checkout -b feature/nouvelle-question-qcm

# Faire vos modifications
# Tester localement avec: npm run dev

# Ajouter et committer
git add .
git commit -m "Ajout: Nouvelle question sur les API REST"

# Pousser la branche
git push -u origin feature/nouvelle-question-qcm
```

### 2. Mise en Production
```bash
# Retourner sur la branche main
git checkout main

# Fusionner votre branche
git merge feature/nouvelle-question-qcm

# Pousser vers GitHub (déclenchera le redéploiement Netlify)
git push
```

### 3. Nettoyage
```bash
# Supprimer la branche locale
git branch -d feature/nouvelle-question-qcm

# Supprimer la branche distante
git push origin --delete feature/nouvelle-question-qcm
```

## 🎓 Bonnes Pratiques

1. **Commits fréquents** : Faites des commits réguliers avec des messages clairs
2. **Branches pour les fonctionnalités** : Utilisez des branches pour chaque nouvelle fonctionnalité
3. **Pull avant Push** : Toujours faire `git pull` avant `git push`
4. **Messages descriptifs** : Écrivez des messages de commit qui expliquent le "pourquoi"
5. **Testez avant de committer** : Vérifiez que tout fonctionne localement

## 📖 Ressources

- Documentation Git : https://git-scm.com/doc
- GitHub Guides : https://guides.github.com
- Tutoriel interactif : https://learngitbranching.js.org

---

**Auteur** : Eric MORMIN  
**Organisation** : EKM Conseils  
**Date** : Janvier 2026
