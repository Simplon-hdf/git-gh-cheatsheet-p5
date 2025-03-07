# 🛠 Git - Guide des Branches

## Introduction aux branches

- [Créer et basculer entre les branches](#🏗️-créer-et-basculer-entre-les-branches)
- [Fusionner des branches](#🔀-fusionner-des-branches)
- [Gérer les conflits de merge](#⚠️-gérer-les-conflits-de-merge)
- [Envoyer des modifications vers un dépôt distant](#🚀-envoyer-des-modifications-vers-un-dépôt-distant)
- [Notes d'utilisation](#📝-notes-dutilisation)

### Concept de branche

```bash
git branch                          # Affiche toutes les branches locales
```

Git permet de gérer les branches pour travailler sur plusieurs fonctionnalités ou correctifs en parallèle. Chaque branche est un environnement indépendant où les développeurs peuvent effectuer des modifications sans perturber le travail des autres. La branche principale est souvent appelée main ou master, mais des branches spécifiques peuvent être créées pour développer de nouvelles fonctionnalités, corriger des bugs ou expérimenter.

## 🏗️ Créer et basculer entre les branches

### Création d'une branche

```bash
git branch <nom_branche>           # Crée une nouvelle branche sans y basculer
```

Options disponibles :

```bash
git branch -v                      # Affiche les branches locales avec le dernier commit sur chaque branche
git branch --merged                # Affiche les branches qui ont été fusionnées dans la branche courante
git branch --no-merged             # Affiche les branches qui n'ont pas été fusionnées dans la branche courante
```

### Basculer entre branches

```bash
git checkout <nom_branche>         # Change la branche courante pour nom_branche
```

Options disponibles :

```bash
git checkout -b <nom_branche>      # Crée une nouvelle branche nommée nom_branche et se déplace dessus
git switch <nom_branche>           # Change la branche courante pour nom_branche (équivalent à git checkout <nom_branche>)
git switch -c <nom_branche>        # Crée une nouvelle branche nommée nom_branche et se déplace dessus (équivalent à git checkout -b <nom_branche>)
```

## 🔀 Fusionner des branches

### Merge

```bash
git merge <branche_source>         # Fusionne la branche branche_source dans la branche courante
```

Options disponibles :

```bash
git merge --no-ff <branche>        # Fusionne la branche dans la branche courante en créant un commit de fusion, même en cas de fast-forward
git merge --abort                  # Annule un merge en cours et revient à l'état avant le début du merge
```

### Rebase

```bash
git rebase <branche_source>        # Rebase la branche courante sur la branche branche_source
```

Options disponibles :

```bash
git rebase --continue              # Continue un rebase après résolution de conflits
git rebase --abort                 # Annule un rebase en cours et revient à l'état avant le début du rebase
git rebase -i HEAD~<n>             # Lance un rebase interactif sur les n derniers commits à partir de HEAD
```

## ⚠️ Gérer les conflits de merge

### Résolution de conflits

```bash
git status                         # Affiche l'état actuel de l'arbre de travail et de l'index (fichiers modifiés, en attente de commit, etc.)
```

Options disponibles :

```bash
git add <fichiers_conflits>        # Ajoute les fichiers spécifiés à l'index après résolution des conflits
git commit                         # Termine la fusion après résolution des conflits / Enregistre les modifications de l'index dans l'historique des commits
git mergetool                      # Ouvre un outil de fusion graphique pour aider à résoudre les conflits
```

## 🚀 Envoyer des modifications vers un dépôt distant

### Push

```bash
git push origin <nom_branche>      # Envoie la branche locale vers le dépôt distant
```

Options disponibles :

```bash
git push --all origin              # Pousse toutes les branches locales vers le dépôt distant origin
git push --force                   # FForce la mise à jour du dépôt distant avec les modifications locales, même si cela écrase les modifications distantes.
git push -u origin <branche>       # Pousse la branche locale branche vers origin et la définit comme la branche de suivi par défaut
```

## Récupérer les modifications d'un dépôt distant

### Pull

```bash
git pull                           # Récupère les modifications du dépôt distant et les fusionne dans la branche locale courante
```

Options disponibles :

```bash
git pull --rebase                  # Récupère les modifications du dépôt distant et les applique sur la branche locale courante via un rebase
git fetch                          # Télécharge les objets et les références depuis un autre dépôt
git fetch --all                    # Télécharge les objets et les références depuis tous les dépôts distants configurés
```

## Travailler avec des forks et des pull requests

### Gestion des forks

```bash
git remote add upstream <url>      # Ajoute un dépôt distant nommé upstream avec l'URL spécifiée
```

Options disponibles :

```bash
git fetch upstream                 # Télécharge les objets et les références depuis le dépôt distant upstream
git merge upstream/main            # Fusionne la branche main du dépôt distant upstream dans la branche locale courante.
git pull upstream main             # Récupère les modifications de la branche main du dépôt distant upstream et les fusionne dans la branche locale courante
```

## 📝 Notes d'utilisation

### Format des commandes

- < > : paramètre optionnel

### Bonnes pratiques

- Créez des branches pour chaque nouvelle fonctionnalité ou correctif
- Utilisez des noms de branches descriptifs (feature/nom-fonctionnalité, bugfix/problème)
- Synchronisez régulièrement vos branches avec la branche principale
- Préférez le rebase pour garder un historique propre avant de fusionner dans main/master

### Points de vigilance

- Utilisez `git push --force` avec précaution car cela peut effacer le travail d'autres personnes
- Résolvez toujours complètement les conflits avant de terminer un merge/rebase
- N'utilisez pas rebase sur des branches partagées/publiées
- Vérifiez toujours que vous êtes sur la bonne branche avant de commencer à travailler
