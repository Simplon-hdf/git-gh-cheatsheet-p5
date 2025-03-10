# GitHub CLI - Guide des Commandes

## Table des matières
- [Gestion des actions](#gestion-des-actions)
- [Gestion des workflows](#gestion-des-workflows)
- [Gestion des Jobs et Runs](#gestion-des-jobs-et-runs)
- [Notes d'utilisation](#notes-dutilisation)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Gestion des actions
### 📦 Lister les actions disponibles
```bash
gh actions list # Lister toutes les actions disponibles dans le dépôt courant
```
Options disponibles :
```bash
gh actions list --workflow [workflow] # Lister les actions d'un workflow spécifique
gh actions list --job [nom-job] # Lister les actions pour un job spécifique
```

### ⬇️ Télécharger une action
```bash
gh actions download [action] # Télécharger une action spécifique du dépôt courant
```
Options disponibles :
```bash
gh actions download [action] --path [répertoire] # Spécifier le répertoire pour enregistrer l'action
```

## Gestion des workflows
### 📋 Lister les workflows
```bash
gh workflow list # Lister tous les workflows dans le dépôt courant
```
Options disponibles :
```bash
gh workflow list --state [état] # Filtrer par état (enabled, disabled, etc.)
gh workflow list --trigger [trigger] # Filtrer par déclencheur (push, pull_request, etc.)
```

### ▶️ Exécuter un workflow
```bash
gh workflow run [nom-workflow] # Lancer manuellement un workflow spécifique
```
Options disponibles :
```bash
gh workflow run [nom-workflow] --ref [branche] # Spécifier une branche ou un commit pour le workflow
gh workflow run [nom-workflow] --inputs "[paramètres]" # Passer des paramètres d'entrée au workflow
```

### 🔄 Activer/Désactiver un workflow
```bash
gh workflow enable [nom-workflow] # Activer un workflow
```
Options disponibles :
```bash
gh workflow disable [nom-workflow] # Désactiver un workflow
```

## Gestion des Jobs et Runs
### 📊 Lister les runs d'un workflow
```bash
gh run list # Lister les runs des workflows dans le dépôt courant
```
Options disponibles :
```bash
gh run list --workflow [nom-workflow] # Filtrer par workflow spécifique
gh run list --status [status] # Filtrer par état (success, failure, etc.)
gh run list --actor [utilisateur] # Filtrer par utilisateur ayant lancé le run
```

### 🔍 Afficher un run spécifique
```bash
gh run view [ID-run] # Afficher les détails d'un run spécifique
```
Options disponibles :
```bash
gh run view [ID-run] --log # Afficher les logs détaillés du run
gh run view [ID-run] --json # Afficher les détails en format JSON
```

### ⏹️ Annuler un run en cours
```bash
gh run cancel [ID-run] # Annuler un run en cours
```
Options disponibles :
```bash
gh run cancel [ID-run] --force # Annuler un run immédiatement, même s'il est en cours
```

## Notes d'utilisation
### 📝 Format des commandes
- [paramètre] : paramètre obligatoire


### ✨ Bonnes pratiques
- Utilisez des workflows YAML clairs et concis pour une meilleure lisibilité.
- Testez les workflows dans un environnement de développement avant de les appliquer en production.
- Utilisez les paramètres d'entrée pour personnaliser l'exécution des workflows et améliorer leur réutilisabilité.

### ⚠️ Points de vigilance
- Soyez prudent avec l'activation et la désactivation des workflows, car cela peut affecter l'automatisation de votre projet.
- Vérifiez que les paramètres d'entrée sont correctement configurés pour éviter des erreurs dans les workflows.
- Faites attention à la gestion des secrets dans les workflows afin de ne pas exposer des informations sensibles.

## Pour aller plus loin
**### 📚 Documentation officielle**
- [Documentation GitHub CLI](https://cli.github.com/manual/)
- [Guide de démarrage rapide](https://docs.github.com/en/github-cli/github-cli/quickstart)
- [FAQ GitHub CLI](https://cli.github.com/manual/gh_help_reference)

**### 👥 Communauté**
- [GitHub Community Forum](https://github.community/)
- [Stack Overflow [github-cli]](https://stackoverflow.com/questions/tagged/github-cli)
- [GitHub Discussions](https://github.com/cli/cli/discussions)