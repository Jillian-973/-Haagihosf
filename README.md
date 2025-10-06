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

## 📌 Ressources utiles

- [Documentation Git](https://git-scm.com/doc)
- [Documentation GitHub](https://docs.github.com/)
- [GitHub Flow Guide](https://guides.github.com/introduction/flow/)
- [VS Code Git Integration](https://code.visualstudio.com/docs/editor/versioncontrol)

---

## ✍️ Auteur

**Jillian-973**

📅 **Créé le :** 2025