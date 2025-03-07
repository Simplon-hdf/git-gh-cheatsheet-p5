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
