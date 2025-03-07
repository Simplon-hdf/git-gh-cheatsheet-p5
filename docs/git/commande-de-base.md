# 🛠 [Git] - Guide des Commandes

## 📑 Table des matières
- [Commande de base](#Commande-de-base)
- [Notes d'utilisation](#notes-dutilisation)

## Commande de base

### git init
```bash
git init              # Crée ou réinitialise un dépôt Git
```

Options disponibles :
```bash
git init [--bare]              # Crée un dépot Git sans working directory
git init [--quiet]              # Affiche seulement les messages d'erreur.
git init [-b] <nom de la branche>             # Choisir le nom de la première branche
```

### git add
```bash
git add              # Ajoute un ou plusieurs fichier(s) dans la zone de staging.
```

Options disponibles :
```bash
git add ["nom du fichier 1"] <"nom du fichier 2">              # Ajoute les fichiers en options
git add [*]              # Ajoute tous les fichiers non cachés
git add [.]              # Ajoute tous les fichiers
```

### git commit
```bash
git commit              # Crée un nouveau commit
```

Options disponibles :
```bash
git commit [-m] <"message">              # Ajoute un message au commit
git commit [-am] <"message">              # Ajoute à la zone de staging et commit tous les fichiers qui ont des changements
git commit [-amend] [-m] <"message">            # Permet de modifier le dernier commit
git commit [-amend] [--no-edit]            # modifier sans changer le message
```

## git status
```bash
git status              # Permet de montré quel fichier dans la zone de staging
```

Options disponibles :
```bash
git status [-s] | [--short]             # Montre une version simplifié
git status [---ignored]            # Montre les fichiers ignorés
git status [-amend] [-m] <"message">            # Permet de modifier le dernier commit
git status [-u] [no] | [all]            # Ne montre pas les fichiers non suivis | Voir tous les fichiers"
```
### git log

```bash
git log              # Affiche l'historique des commits
```

Options disponibles :
```bash
git log [--oneline]              # Affiche chaque commit sur une seule ligne (hash + message)
git log [--graph]                # Affiche un graphe ASCII de l'historique des branches
git log [--author="Nom"]         # Filtre les commits par auteur
git log [--since="YYYY-MM-DD"]   # Affiche les commits depuis une date donnée
git log [--grep="fix"]           # Recherche des commits contenant un mot-clé dans le message
git log [-p]                     # Affiche les différences (patch) pour chaque commit
git log [--stat]                 # Affiche un résumé des fichiers modifiés
```


## 📝 Notes d'utilisation

### Format des commandes
- [ ] : paramètre obligatoire
- < > : paramètre optionnel
- | : choix entre plusieurs options

### Bonnes pratiques
- [Conseil d'utilisation 1]
- [Conseil d'utilisation 2]
- [Conseil d'utilisation 3]

### Points de vigilance
- [Avertissement 1]
- [Avertissement 2]
- [Avertissement 3]

