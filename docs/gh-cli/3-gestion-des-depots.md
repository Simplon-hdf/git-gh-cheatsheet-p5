# GitHub CLI - Guide des Commandes

## Table des matières
- [Gestion des dépôts](#gestion-des-dépôts)
- [Gestion des issues](#gestion-des-issues)
- [Gestion des pull requests](#gestion-des-pull-requests)
- [Notes d'utilisation](#notes-dutilisation)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Gestion des dépôts
### 📥 Cloner un dépôt
```bash
gh repo clone [utilisateur]/[dépôt] # Clone un dépôt GitHub localement sur l'ordinateur
```
Options disponibles :
```bash
gh repo clone [utilisateur]/[dépôt] --branch [nom-branche] # Clone une branche spécifique du dépôt
gh repo clone [utilisateur]/[dépôt] --depth [profondeur] # Cloner un dépôt avec un historique d'une certaine profondeur
gh repo clone [utilisateur]/[dépôt] --quiet # Cloner sans afficher de sortie
```

### 🆕 Créer un dépôt
```bash
gh repo create [nom-dépôt] # Créer un nouveau dépôt sur GitHub
```
Options disponibles :
```bash
gh repo create [nom-dépôt] --public # Créer un dépôt public
gh repo create [nom-dépôt] --private # Créer un dépôt privé
gh repo create [nom-dépôt] --description "<description>" # Ajouter une description au dépôt
```

## Gestion des issues
### ➕ Créer une issue
```bash
gh issue create # Crée une nouvelle issue sur le dépôt courant
```
Options disponibles :
```bash
gh issue create --title "[Titre]" # Créer une issue avec un titre spécifique
gh issue create --body "[Description]" # Créer une issue avec une description spécifique
gh issue create --label "[étiquette]" # Ajouter une étiquette à l'issue
```

### 📋 Lister les issues
```bash
gh issue list # Lister les issues ouvertes dans le dépôt courant
```
Options disponibles :
```bash
gh issue list --state [état] # Filtrer par état (open, closed, etc.)
gh issue list --label "[étiquette]" # Filtrer par étiquette
gh issue list --assignee "[utilisateur]" # Filtrer par assigné
```

## Gestion des pull requests
### 🔄 Créer une pull request
```bash
gh pr create # Créer une pull request à partir de la branche actuelle
```
Options disponibles :
```bash
gh pr create --base [branche-cible] # Créer une PR vers une branche spécifique
gh pr create --title "[Titre]" # Ajouter un titre à la PR
gh pr create --body "[Description]" # Ajouter une description à la PR
```

### 📊 Lister les pull requests
```bash
gh pr list # Lister les pull requests ouvertes
```
Options disponibles :
```bash
gh pr list --state [état] # Filtrer par état (open, closed, merged)
gh pr list --assignee "[utilisateur]" # Filtrer par assigné
gh pr list --label "[étiquette]" # Filtrer par étiquette
```

## Notes d'utilisation
### 📝 Format des commandes
- [paramètre] : paramètre obligatoire.


### ✨ Bonnes pratiques
- Utilisez des branches pour chaque nouvelle fonctionnalité ou correction.
- Utilisez des titres clairs et descriptifs pour les issues et PR.
- Mettez à jour les étiquettes de manière cohérente pour faciliter le tri.

### ⚠️ Points de vigilance
- Vérifiez les conflits de fusion lors de la création de PR.
- Soyez prudent lors de la suppression de dépôts, cela est irréversible.
- Ne partagez jamais vos tokens d'accès ou vos informations sensibles.

## Pour aller plus loin
### 📚 Documentation officielle
- [Documentation GitHub CLI](https://cli.github.com/manual/)
- [Guide de démarrage rapide](https://docs.github.com/en/github-cli/github-cli/quickstart)
- [FAQ GitHub CLI](https://cli.github.com/manual/gh_help_reference)

### 👥 Communauté
- [GitHub Community Forum](https://github.community/)
- [Stack Overflow [github-cli]](https://stackoverflow.com/questions/tagged/github-cli)
- [GitHub Discussions](https://github.com/cli/cli/discussions)

