# GitHub CLI - Commandes Supplémentaires


- [GitHub CLI - Commandes Supplémentaires](#github-cli---commandes-supplémentaires)
  - [Configuration et personnalisation](#configuration-et-personnalisation)
    - [🔄 gh alias](#-gh-alias)
    - [🔄 gh completion](#-gh-completion)
    - [⚙️ gh config](#️-gh-config)
  - [Gestion des authentifications](#gestion-des-authentifications)
    - [🔑 gh gpg-key](#-gh-gpg-key)
    - [🔑 gh ssh-key](#-gh-ssh-key)
  - [Interaction avec l'API](#interaction-avec-lapi)
    - [🌐 gh api](#-gh-api)
    - [✅ gh attestation](#-gh-attestation)
  - [Organisation et métadonnées](#organisation-et-métadonnées)
    - [🏷️ gh label](#️-gh-label)
    - [📋 gh ruleset](#-gh-ruleset)
    - [🔒 gh secret](#-gh-secret)
    - [🔧 gh variable](#-gh-variable)
  - [Recherche et statut](#recherche-et-statut)
    - [🔍 gh search](#-gh-search)
    - [📊 gh status](#-gh-status)
  - [Notes d'utilisation](#notes-dutilisation)
    - [📝 Format des commandes](#-format-des-commandes)
  - [Pour aller plus loin](#pour-aller-plus-loin)
    - [📚 Documentation officielle](#-documentation-officielle)
    - [👥 Communauté](#-communauté)
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

### 🔑 gh ssh-key
```bash
gh ssh-key                         # Gérer les clés SSH associées à votre compte GitHub
```
Options disponibles :
```bash
gh ssh-key [add] [fichier_clé] <options>    # Ajouter une nouvelle clé SSH à votre compte GitHub
gh ssh-key [list] <options>                 # Lister les clés SSH actuellement associées à votre compte
gh ssh-key [delete] [clé_id] <options>      # Supprimer une clé SSH de votre compte GitHub
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

### ✅ gh attestation
```bash
gh attestation                     # Gérer les attestations d'artefacts dans GitHub Actions
```
Options disponibles :
```bash
gh attestation [download] [artefact]  # Télécharger les attestations associées à un artefact
gh attestation [verify] [artefact]    # Vérifier l'intégrité et l'authenticité d'un artefact
gh attestation [trusted-root]         # Afficher le fichier `trusted_root.jsonl` pour une vérification hors ligne
```

## Organisation et métadonnées
### 🏷️ gh label
```bash
gh label                           # Gérer les labels dans un dépôt GitHub
```
Options disponibles :
```bash
gh label [clone] [source_repo] <options>  # Cloner les labels d'un dépôt source vers un dépôt cible
gh label [create] [nom] <options>         # Créer un nouveau label dans le dépôt
gh label [delete] [nom] <options>         # Supprimer un label existant du dépôt
gh label [edit] [nom] <options>           # Modifier un label existant dans le dépôt
gh label [list] <options>                 # Lister tous les labels du dépôt
```

### 📋 gh ruleset
```bash
gh ruleset                         # Gérer les ensembles de règles dans un dépôt GitHub
```
Options disponibles :
```bash
gh ruleset [check] [branche] [options]  # Vérifier les règles qui s'appliquent à une branche spécifique
gh ruleset [list] [options]             # Lister les ensembles de règles pour un dépôt ou une organisation
gh ruleset [view] [ID] [options]        # Afficher les détails d'un ensemble de règles spécifique
```

### 🔒 gh secret
```bash
gh secret                          # Gérer les secrets GitHub au niveau du dépôt, de l'organisation ou de l'utilisateur
```
Options disponibles :
```bash
gh secret [set] [nom] <options>      # Créer ou mettre à jour un secret
gh secret [list] <options>           # Lister les secrets existants
gh secret [remove] [nom] <options>   # Supprimer un secret
```

### 🔧 gh variable
```bash
gh variable                        # Gérer les variables GitHub pour les workflows Actions
```
Options disponibles :
```bash
gh variable [set] [nom] <options>    # Créer ou mettre à jour une variable
gh variable [list] <options>         # Lister les variables existantes
gh variable [delete] [nom] <options> # Supprimer une variable
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
gh search [prs] [mot-clé] <options>      # Rechercher des pull requests correspondant à des mots-clés
gh search [code] [mot-clé] <options>     # Rechercher du code correspondant à des mots-clés
gh search [commits] [mot-clé] <options>  # Rechercher des commits correspondant à des mots-clés
```

### 📊 gh status
```bash
gh status                          # Afficher un aperçu des activités récentes sur GitHub
```
Options disponibles :
```bash
gh status [-e] | [--exclude] [repo] <repo2>     # Exclure un ou plusieurs dépôts spécifiques des résultats
gh status [-o],| [--org] [organisation>]   # Limiter les résultats à une organisation spécifique
```

## Notes d'utilisation
### 📝 Format des commandes
- [paramètre] : paramètre obligatoire
- < > : paramètre optionnel
- | : choix entre plusieurs options

## Pour aller plus loin
### 📚 Documentation officielle
- [Documentation GitHub CLI](https://cli.github.com/manual/)
- [Guide de démarrage rapide](https://docs.github.com/en/github-cli/github-cli/quickstart)
- [FAQ GitHub CLI](https://cli.github.com/manual/gh_help_reference)

### 👥 Communauté
- [GitHub Community Forum](https://github.community/)
- [Stack Overflow [github-cli]](https://stackoverflow.com/questions/tagged/github-cli)
- [GitHub Discussions](https://github.com/cli/cli/discussions)