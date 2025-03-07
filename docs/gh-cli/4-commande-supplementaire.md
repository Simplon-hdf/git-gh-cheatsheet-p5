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

