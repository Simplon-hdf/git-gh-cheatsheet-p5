# 📘 GitHub CLI

## 📑 Table des matières

- [Commande supplementaire](#commande-de-base)
- [Notes d'utilisation](#📝-notes-dutilisation)

## Commande supplementaire

### gh alias
```bash
gh alias                           # Gérer les alias pour la CLI GitHub
```

Options disponibles :

```bash
gh alias [list]                      # Afficher tous les alias définis
gh alias [set] [alias] [commande]    # Créer un alias pour la commande
gh alias [delete] [alias]            # Supprimer un alias existant
```

### gh api
```bash
gh api                             # Effectuer des requêtes authentifiées vers l'API GitHub.

```

Options disponibles :

```bash
gh api [endpoint]                  # Effectuer une requête GET sur l'endpoint spécifié
gh api [-X] [méthode] [endpoint]     # Spécifier la méthode HTTP à utiliser : GET, POST, PUT, DELETE, PATCH
gh api [--hostname] [nom_hôte] [endpoint]  # Spécifier l'hôte GitHub à utiliser (par défaut : github.com)

```

### gh attestation
```bash
gh attestation                     # Gérer les attestations d'artefacts dans GitHub Actions

```

Options disponibles :

```bash
gh attestation [download] [artefact]  # Télécharger les attestations associées à un artefact
gh attestation [verify] [artefact]    # Vérifier l'intégrité et l'authenticité d'un artefact
gh attestation [trusted-root]         # Afficher le fichier `trusted_root.jsonl` pour une vérification hors ligne

```

### gh completion
```bash
gh completion -s <shell>           # Génère des scripts de complétion pour le shell spécifié

```

Options disponibles :

```bash
gh completion [-s] [bash]              # Génère un script de complétion pour Bash
gh completion [-s] [zsh]               # Génère un script de complétion pour Zsh
gh completion [-s] [fish]              # Génère un script de complétion pour Fish

```
### gh config
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

### gh gpg-key
```bash
gh gpg-key                         # Gérer les clés GPG enregistrées dans votre compte GitHub

```

Options disponibles :

```bash
gh gpg-key [add] [chemin_clé]        # Ajouter une clé GPG à votre compte GitHub
gh gpg-key [list]                    # Lister les clés GPG enregistrées dans votre compte
gh gpg-key [delete] [clé_id]         # Supprimer une clé GPG de votre compte GitHub

```

### gh label
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

### gh ruleset
```bash
gh ruleset                         # Gérer les ensembles de règles dans un dépôt GitHub

```

Options disponibles :

```bash
gh ruleset [check] [branche] [options]  # Vérifier les règles qui s'appliquent à une branche spécifique
gh ruleset [list] [options]             # Lister les ensembles de règles pour un dépôt ou une organisation
gh ruleset [view] [ID] [options]        # Afficher les détails d'un ensemble de règles spécifique

```

### gh search
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

### gh secret
```bash
gh secret                          # Gérer les secrets GitHub au niveau du dépôt, de l'organisation ou de l'utilisateur

```

Options disponibles :

```bash
gh secret [set] [nom] <options>      # Créer ou mettre à jour un secret
gh secret [list] <options>           # Lister les secrets existants
gh secret [remove] [nom] <options>   # Supprimer un secret

```
### gh ssh-key
```bash
gh ssh-key                         # Gérer les clés SSH associées à votre compte GitHub


```

Options disponibles :

```bash
gh ssh-key [add] [fichier_clé] <options>    # Ajouter une nouvelle clé SSH à votre compte GitHub
gh ssh-key [list] <options>                 # Lister les clés SSH actuellement associées à votre compte
gh ssh-key [delete] [clé_id] <options>      # Supprimer une clé SSH de votre compte GitHub

```




