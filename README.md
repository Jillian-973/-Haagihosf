# 📌 Projet Haagihosf

Bienvenue dans le projet **Haagihosf** 🎉  
Ce dépôt contient le code source ainsi que toutes les instructions pour configurer, exécuter et collaborer sur ce projet à l'aide de **Git** et **Visual Studio Code (VS Code)**.

---

## 🚀 Prérequis

Avant de commencer, assure-toi d'avoir installé :

- [Git](https://git-scm.com/) (gestion de version)  
- [Visual Studio Code](https://code.visualstudio.com/) (éditeur de code)  
- Un compte [GitHub](https://github.com/)  

---

## 📥 Installation et clonage

Cloner ce projet sur votre machine locale :

```bash
git clone https://github.com/Jillian-973/-Haagihosf.git
cd -Haagihosf
```

---

## 🔗 Utilisation avec Visual Studio Code

1. **Ouvrir Visual Studio Code**
   - Menu **File** → **Open Folder** → sélectionner le dossier du projet

2. **Vérifier que Git est actif dans VS Code** (icône Source Control dans la barre latérale)

3. **Se connecter à GitHub depuis VS Code** (onglet Accounts en bas à gauche)

4. Vous pouvez gérer vos commits, push et pull directement depuis l'onglet **Source Control** ou via le terminal intégré

---

## 💾 Commandes Git essentielles

### Initialiser un repo (si nécessaire)
```bash
git init
git branch -M main
git remote add origin https://github.com/Jillian-973/-Haagihosf.git
```

### Sauvegarder vos changements
```bash
git add .
git commit -m "Message de commit clair"
```

### Envoyer vos changements sur GitHub
```bash
git push origin main
```

### Récupérer les changements du dépôt distant
```bash
git pull origin main
```

⚠️ **Si vous obtenez l'erreur `rejected (fetch first)` :**

```bash
git pull origin main --rebase
git push origin main
```

---

## 👥 Collaboration

### Pour ajouter un collaborateur :
**GitHub** → **Settings** → **Collaborators** → Ajouter le pseudo GitHub de la personne

### Workflow recommandé :

1. **Créer une branche pour vos modifications :**
   ```bash
   git checkout -b feature-ma-fonctionnalite
   ```

2. **Commit + Push vos changements**

3. **Créer une Pull Request sur GitHub**

4. Un collaborateur valide la PR avant fusion dans `main`

---

## 📂 Structure du projet (exemple)

```
Haagihosf/
│
├── src/            # Code source
├── docs/           # Documentation
├── tests/          # Tests unitaires
├── .gitignore      # Fichiers à ignorer par Git
└── README.md       # Documentation principale
```

---

## 🛠 Bonnes pratiques Git

- Faire des commits petits et fréquents avec des messages clairs
- Toujours `pull` avant de commencer à coder
- Utiliser des branches pour chaque nouvelle fonctionnalité
- Passer par des Pull Requests pour valider le code
- Ne jamais forcer un push sauf si vous êtes absolument sûr

---

## ❓ FAQ : Erreurs fréquentes

### 🔴 `error: failed to push some refs`
➡️ **Solution :**
```bash
git pull origin main --rebase
git push origin main
```

### 🔴 Merge conflict
➡️ Ouvrir les fichiers concernés dans VS Code, choisir les bonnes lignes (**Accept Current Change** ou **Accept Incoming Change**), puis :
```bash
git add .
git commit
git push
```

### 🔴 HEAD détaché (detached HEAD)
➡️ Retourner sur la branche principale :
```bash
git checkout main
```

---
# 🌿 Guide complet - Gestion des branches Git

Ce guide vous explique étape par étape comment créer, utiliser et fusionner des branches avec Git.

---

## 📚 Table des matières

1. [Créer une branche](#1--créer-une-branche)
2. [Changer de branche](#2--changer-de-branche)
3. [Travailler et push dans une branche](#3--travailler-et-push-dans-une-branche)
4. [Fusionner (merge) une branche dans main](#4--fusionner-merge-une-branche-dans-main)
5. [Supprimer une branche](#5--supprimer-une-branche)
6. [Commandes utiles](#6--commandes-utiles)

---

## 1. 🌱 Créer une branche

### Créer et basculer directement sur la nouvelle branche
```bash
git checkout -b nom-de-la-branche
```

**Exemple :**
```bash
git checkout -b feature-login
```

### Ou créer sans basculer dessus
```bash
git branch nom-de-la-branche
```

### ✅ Vérifier la création
```bash
git branch
```
La branche active est marquée avec un astérisque `*`

---

## 2. 🔄 Changer de branche

### Basculer vers une branche existante
```bash
git checkout nom-de-la-branche
```

**Exemple :**
```bash
git checkout blog
```

### Méthode alternative (Git 2.23+)
```bash
git switch nom-de-la-branche
```

### ⚠️ Important
Avant de changer de branche, assurez-vous que :
- Tous vos fichiers sont commités **OU**
- Vous utilisez `git stash` pour sauvegarder temporairement vos modifications

```bash
# Sauvegarder temporairement les modifications
git stash

# Changer de branche
git checkout autre-branche

# Récupérer les modifications
git stash pop
```

---

## 3. 💾 Travailler et push dans une branche

### Étape 1 : Vérifier que vous êtes sur la bonne branche
```bash
git branch
```

### Étape 2 : Faire vos modifications
Éditez vos fichiers avec VS Code ou votre éditeur préféré

### Étape 3 : Ajouter les fichiers modifiés
```bash
# Ajouter tous les fichiers modifiés
git add .

# Ou ajouter un fichier spécifique
git add nom-du-fichier.txt
```

### Étape 4 : Commiter vos changements
```bash
git commit -m "Description claire des modifications"
```

**Exemple :**
```bash
git commit -m "Ajout de la page de connexion"
```

### Étape 5 : Pousser la branche sur GitHub
```bash
git push origin nom-de-la-branche
```

**Exemple :**
```bash
git push origin feature-login
```

### 🆕 Premier push d'une nouvelle branche
Si c'est la première fois que vous poussez cette branche :
```bash
git push -u origin nom-de-la-branche
```

L'option `-u` (upstream) configure le suivi automatique de la branche distante.

---

## 4. 🔀 Fusionner (merge) une branche dans main

### Méthode 1 : Merge en ligne de commande (local)

#### Étape 1 : Basculer sur la branche main
```bash
git checkout main
```

#### Étape 2 : Mettre à jour main
```bash
git pull origin main
```

#### Étape 3 : Fusionner votre branche dans main
```bash
git merge nom-de-la-branche
```

**Exemple :**
```bash
git merge feature-login
```

#### Étape 4 : Pousser les modifications
```bash
git push origin main
```

### Méthode 2 : Pull Request sur GitHub (recommandée) 🌟

#### Étape 1 : Pousser votre branche sur GitHub
```bash
git push origin nom-de-la-branche
```

#### Étape 2 : Créer une Pull Request
1. Aller sur GitHub : `https://github.com/votre-username/votre-repo`
2. Cliquer sur **"Compare & pull request"** (bouton jaune qui apparaît)
3. Ajouter un titre et une description
4. Cliquer sur **"Create pull request"**

#### Étape 3 : Révision et merge
1. Un collaborateur (ou vous-même) révise le code
2. Cliquer sur **"Merge pull request"**
3. Confirmer avec **"Confirm merge"**

#### Étape 4 : Mettre à jour votre branche main locale
```bash
git checkout main
git pull origin main
```

---

## 5. 🗑️ Supprimer une branche

### Supprimer une branche locale (après merge)
```bash
git branch -d nom-de-la-branche
```

### Forcer la suppression (si pas mergée)
```bash
git branch -D nom-de-la-branche
```

### Supprimer une branche distante (sur GitHub)
```bash
git push origin --delete nom-de-la-branche
```

---

## 6. 🛠️ Commandes utiles

### Lister toutes les branches
```bash
# Branches locales
git branch

# Branches distantes
git branch -r

# Toutes les branches
git branch -a
```

### Voir l'historique des commits
```bash
git log --oneline --graph --all
```

### Voir les différences entre branches
```bash
git diff main..nom-de-la-branche
```

### Renommer une branche
```bash
# Renommer la branche actuelle
git branch -m nouveau-nom

# Renommer une autre branche
git branch -m ancien-nom nouveau-nom
```

---

## 📋 Workflow complet - Exemple pratique

```bash
# 1. Créer et basculer sur une nouvelle branche
git checkout -b feature-newsletter

# 2. Faire des modifications dans vos fichiers
# ... éditer les fichiers ...

# 3. Ajouter et commiter
git add .
git commit -m "Ajout du formulaire d'inscription newsletter"

# 4. Pousser la branche sur GitHub
git push -u origin feature-newsletter

# 5. Créer une Pull Request sur GitHub (via l'interface web)

# 6. Après validation, basculer sur main
git checkout main

# 7. Mettre à jour main
git pull origin main

# 8. (Optionnel) Supprimer la branche locale
git branch -d feature-newsletter
```

---

## ⚠️ Résolution de conflits

Si vous rencontrez un conflit lors du merge :

```bash
# 1. Git vous indique les fichiers en conflit
git status

# 2. Ouvrir les fichiers dans VS Code
# Choisir les bonnes modifications (Accept Current/Incoming/Both)

# 3. Ajouter les fichiers résolus
git add .

# 4. Finaliser le merge
git commit -m "Résolution des conflits"

# 5. Pousser
git push origin main
```

---

## 🎯 Bonnes pratiques

✅ **Nommer clairement vos branches** : `feature/`, `bugfix/`, `hotfix/`
- Exemple : `feature/login`, `bugfix/navbar`, `hotfix/security`

✅ **Faire des commits fréquents** avec des messages clairs

✅ **Toujours pull avant de merger** pour éviter les conflits

✅ **Utiliser des Pull Requests** pour la revue de code

✅ **Supprimer les branches** après le merge pour garder le repo propre

❌ **Ne jamais travailler directement sur main** (sauf exception)

---

**Bon courage avec Git ! 🚀**
---

## 📌 Ressources utiles

- [Documentation Git](https://git-scm.com/doc)
- [Documentation GitHub](https://docs.github.com/)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [VS Code Git Integration](https://code.visualstudio.com/docs/editor/versioncontrol)

---

## ✍️ Auteur

**Jillian-973**

📅 **Créé le :** SEPT 2025
