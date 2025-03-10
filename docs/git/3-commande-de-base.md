# Git - Guide des Commandes

## Table des matières
- [Commande de base](#commande-de-base)
- [Notes d'utilisation](#notes-dutilisation)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Commandes de base

### 🔨 git init
```bash
git init # Crée ou réinitialise un dépôt Git
```

Options disponibles :
```bash
git init [--bare] # Crée un dépôt Git sans working directory
git init [--quiet] # Affiche seulement les messages d'erreur
git init [-b] <nom de la branche> # Choisir le nom de la première branche
```

### ➕ git add
```bash
git add ["nom du fichier 1"] # Ajoute un fichier dans la zone de staging
```

Options disponibles :
```bash
git add ["nom du fichier 1"] <"nom du fichier 2"> # Ajoute les fichiers en option
git add [*] # Ajoute tous les fichiers non cachés
git add [.] # Ajoute tous les fichiers
```

### 💾 git commit
```bash
git commit [-m] ["message"] # Crée un nouveau commit avec un message
```

Options disponibles :
```bash
git commit [-m] ["message"] # Ajoute un message au commit
git commit [-am] ["message"] # Ajoute à la zone de staging et commit tous les fichiers qui ont des changements
git commit [--amend] [-m] ["message"] # Permet de modifier le message du dernier commit
git commit [--amend] [--no-edit] # Modifier sans changer le message
```

### 🔍 git status
```bash
git status # Permet de montrer quel fichier dans la zone de staging
```

Options disponibles :
```bash
git status [-s] | [--short] # Montre une version simplifiée
git status [--ignored] # Montre les fichiers ignorés
git status [-u] [no] | [all] # Ne montre pas les fichiers non suivis | Voir tous les fichiers
```

### 📖 git log
```bash
git log # Affiche l'historique des commits
```

Options disponibles :
```bash
git log [--oneline] # Affiche chaque commit sur une seule ligne (hash + message)
git log [--graph] # Affiche un graphe ASCII de l'historique des branches
git log [--author="Nom"] # Filtre les commits par auteur
git log [--since="YYYY-MM-DD"] # Affiche les commits depuis une date donnée
git log [--grep="fix"] # Recherche des commits contenant un mot-clé dans le message
git log [-p] # Affiche les différences (patch) pour chaque commit
git log [--stat] # Affiche un résumé des fichiers modifiés
```

### 🔄 git checkout
```bash
git checkout [commit] # Retourne à un commit spécifique
```

Options disponibles :
```bash
git checkout -b [branche] # Crée une nouvelle branche et bascule dessus
git checkout -b [branche] [commit] # Crée une nouvelle branche à partir d'un commit spécifique
git checkout -f [branche] # Force le changement de branche
git checkout [branche] -- [fichier] # Remplace un fichier dans la branche actuelle par celui d'une autre branche
```

## Notes d'utilisation

### ⌨️ Format des commandes
- [paramètre] : paramètre obligatoire.
- | : choix entre plusieurs options.

### ✅ Bonnes pratiques
- Initialiser le dépôt dans le dossier approprié pour éviter d'avoir des fichiers en trop.
- Vérifier l'état des fichiers avant un commit avec git status.
- Utiliser une convention pour les messages des commits.
- Faire des commits petits et cohérents pour pouvoir se retrouver facilement.

### ⚠️ Points de vigilance
- Ne pas utiliser git commit --amend après un push pour éviter des conflits.
- Ne pas utiliser git add . sans vérifier les fichiers ajoutés pour ne pas commit des fichiers sensibles.

## Pour aller plus loin

### 📚 Documentation officielle
- [git init](https://git-scm.com/docs/git-init) - Documentation complète de git init.
- [git add](https://git-scm.com/docs/git-add) - Documentation complète de git add.
- [git commit](https://git-scm.com/docs/git-commit) - Documentation complète de git commit.
- [git status](https://git-scm.com/docs/git-status) - Documentation complète de git status.
- [git log](https://git-scm.com/docs/git-log) - Documentation complète de git log.
- [git checkout](https://git-scm.com/docs/git-checkout) - Documentation complète de git. checkout

### 🎓 Ressources d'apprentissage
- [Git - Documentation officielle](https://git-scm.com/docs)
- [Pro Git Book](https://git-scm.com/book/fr/v2) - Livre complet sur Git en français.
- [Git Command Explorer](https://gitexplorer.com/) - Outil interactif pour explorer les commandes Git.
- [Oh Shit, Git!?!](https://ohshitgit.com/) - Guide pour résoudre les problèmes Git courants.