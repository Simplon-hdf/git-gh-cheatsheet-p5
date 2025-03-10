# GitHub CLI - Commandes Supplémentaires

## Table des matières
- [GitHub CLI - Commandes Supplémentaires](#github-cli---commandes-supplémentaires)
  - [Table des matières](#table-des-matières)
  - [Configuration et personnalisation](#configuration-et-personnalisation)
  - [Gestion des authentifications](#gestion-des-authentifications)
  - [Interaction avec l'API](#interaction-avec-lapi)
  - [Organisation et métadonnées](#organisation-et-métadonnées)
  - [Recherche et statut](#recherche-et-statut)  
  - [Notes d'utilisation](#notes-dutilisation)
  - [Pour aller plus loin](#pour-aller-plus-loin)
  
## Configuration et personnalisation
### 🔄 gh alias
```bash
gh alias                           # Gérer les alias pour la CLI GitHub
```
Options disponibles :
```bash
gh alias [list]                      # Afficher tous les alias définis
gh alias [set] [alias] [commande]    # Créer un alias pour la commande
gh alias [delete] [alias]            # Supprimer un alias existant
```

### 🔄 gh completion
```bash
gh completion           # Génère des scripts de complétion
```
Options disponibles :
```bash
gh completion [-s] [bash] | [zsh] | [fish]             # Génère un script de complétion pour le shell
```

### ⚙️ gh config
```bash
gh config                          # Afficher ou modifier les paramètres de configuration de gh
```
Options disponibles :
```bash
gh config [get] [clé]                # Afficher la valeur d'une clé de configuration spécifique
gh config [set] [clé] [valeur]       # Définir une valeur pour une clé de configuration spécifique
gh config [list]                     # Afficher toutes les clés de configuration et leurs valeurs
gh config [set] [clé] [valeur] [--host] [hôte]  # Définir une valeur pour une clé de configuration spécifique à un hôte

[clé] = git_protocol | editor | prompt | prefer_editor_prompt | pager | http_unix_socket | browser
```

## Gestion des authentifications
### 🔑 gh gpg-key
```bash
gh gpg-key                         # Gérer les clés GPG enregistrées dans votre compte GitHub
```
Options disponibles :
```bash
gh gpg-key [add] [chemin_clé]        # Ajouter une clé GPG à votre compte GitHub
gh gpg-key [list]                    # Lister les clés GPG enregistrées dans votre compte
gh gpg-key [delete] [clé_id]         # Supprimer une clé GPG de votre compte GitHub
```

## Interaction avec l'API
### 🌐 gh api
```bash
gh api                             # Effectuer des requêtes authentifiées vers l'API GitHub.
```
Options disponibles :
```bash
gh api [endpoint]                  # Effectuer une requête GET sur l'endpoint spécifié
gh api [-X] [méthode] [endpoint]     # Spécifier la méthode HTTP à utiliser : GET, POST, PUT, DELETE, PATCH
gh api [--hostname] [nom_hôte] [endpoint]  # Spécifier l'hôte GitHub à utiliser (par défaut : github.com)
```

## Organisation et métadonnées
### 🌂 gh label
```bash
gh label                           # Gérer les labels dans un dépôt GitHub
```
Options disponibles :
```bash
gh label [clone] [source_repo] <options>  # Cloner les labels d'un dépôt source vers un dépôt cible
gh label [create] [nom] <options>         # Créer un nouveau label dans le dépôt
gh label [delete] [nom] <options>         # Supprimer un label existant du dépôt
```

## Recherche et statut
### 🔍 gh search
```bash
gh search [sous-commande] [arguments] [options]  # Rechercher des dépôts, des issues, des pull requests, du code ou des commits sur GitHub
```
Options disponibles :
```bash
gh search [repos] [mot-clé] <options>    # Rechercher des dépôts correspondant à des mots-clés
gh search [issues] [mot-clé] <options>   # Rechercher des issues correspondant à des mots-clés
```

## Notes d'utilisation
- [paramètre] : paramètre obligatoire
- < > : paramètre optionnel
- | : choix entre plusieurs options

## Pour aller plus loin
### 📚 Documentation officielle
- [Documentation GitHub CLI](https://cli.github.com/manual/)
- [Guide de démarrage rapide](https://docs.github.com/en/github-cli/github-cli/quickstart)

### 👥 Communauté
- [GitHub Community Forum](https://github.community/)
- [Stack Overflow [github-cli]](https://stackoverflow.com/questions/tagged/github-cli)

