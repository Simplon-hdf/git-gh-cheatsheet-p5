## [Commande de retour en arrière]

### [rit reset]
```bash
[git reset]              # [Renvoie la HEAD à un précédent commit]
```

Options disponibles :
```bash
[git reset] [--soft HEAD~X]              # [Annule les X derniers commits en gardant les modifications dans la zone de staging]
[git reset] [--mixed HEAD~X]              # [Annule les X derniers commits et retire les modifications dans la zone de staging]
[git reset] [--hard HEAD~X]              # [Annule les X derniers commits et supprime définitivement les modifications du working directory]
[git reset] [--hard HEAD~X]              # [Annule les X derniers commits et supprime définitivement les modifications du working directory]
[git reset] [commit hash]               # [Retourne la HEAD au commit]
[git reset] [--hard] [commit hash]               # [Retourne la HEAD au commit et supprime les modifications]
[git reset] [--keep] [commit hash]               # [Retourne la HEAD au commit et garde les modifications]
```
