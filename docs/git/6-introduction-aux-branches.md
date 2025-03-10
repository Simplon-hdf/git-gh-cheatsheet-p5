# 🔧 Git - Commandes Avancées

## 📑 Table des matières

- [Git Stash](#🚀-git-stash)
- [Git Diff](#🔍-git-diff)
- [Git Bisect](#🕵️-git-bisect)
- [Git Cherry-Pick](#🍒-git-cherry-pick)
- [Notes d'utilisation](#📝-notes-dutilisation)

## 🚀 Git stash

### Sauvegarder des modifications temporaires

```bash
git stash                          # Stocke les modifications locales dans une réserve temporaire
```

Options disponibles :

```bash
git stash save "message"           # Stocke les modifications avec un message descriptif
git stash -p                       # Mode interactif pour choisir quels changements stocker
git stash --include-untracked      # Inclut également les fichiers non suivis
```

### Gérer les stashs

```bash
git stash list                     # Affiche la liste des stashs enregistrés
```

Options disponibles :

```bash
git stash show stash@{n}           # Affiche les modifications contenues dans le stash spécifié
git stash apply stash@{n}          # Applique un stash spécifique sans le supprimer
git stash pop                      # Applique le dernier stash et le supprime de la liste
git stash drop stash@{n}           # Supprime un stash spécifique
git stash clear                    # Supprime tous les stashs
```

## 🔍 Git diff

### Analyser les différences

```bash
git diff                           # Affiche les modifications non indexées
```

Options disponibles :

```bash
git diff --staged                  # Affiche les modifications indexées (qui seront commises)
git diff HEAD                      # Affiche toutes les modifications depuis le dernier commit
git diff <commit1> <commit2>       # Affiche les différences entre deux commits
git diff <branche1> <branche2>     # Affiche les différences entre deux branches
git diff --stat                    # Affiche un résumé statistique des modifications
```

## 🕵️ Git bisect

### Déboguer avec la recherche binaire

```bash
git bisect start                   # Démarre une session de recherche binaire
```

Options disponibles :

```bash
git bisect bad                     # Marque le commit actuel comme "mauvais" (contient le bug)
git bisect good <commit>           # Marque un commit comme "bon" (sans le bug)
git bisect skip                    # Ignore le commit actuel et passe au suivant
git bisect reset                   # Termine la session de bisect et restaure l'état initial
git bisect run <test_script>       # Exécute un script pour automatiser la recherche
```

## 🧐 Git blame

### Savoir qui a écrit chaque ligne

```bash
git blame [fichier]                # Affiche les auteurs des lignes d'un fichier et leur dernier commit
```

Options disponibles :

```bash
git blame -L [start],[end] [fichier] # Affiche les lignes indiquées
git blame -e [fichier]               # Affiche les informations de l'auteur avec l'email complet
git blame -f [fichier]               # Affiche le nom du fichier avant qu'il ne soit renommé
git blame -M [fichier]               # Détecte les changements de lignes dans les fichiers
```

## 🍒 Git cherry-pick

### Appliquer des commits spécifiques

```bash
git cherry-pick <commit>           # Applique les modifications d'un commit sur la branche actuelle
```

Options disponibles :

```bash
git cherry-pick <commit1> <commit2> # Applique plusieurs commits en séquence
git cherry-pick -n <commit>        # Applique les modifications sans créer de commit
git cherry-pick --continue         # Continue cherry-pick après résolution de conflits
git cherry-pick --abort            # Annule l'opération cherry-pick en cours
git cherry-pick --quit             # Quitte l'opération cherry-pick en conservant les modifications
```

## Git rebase

### Réécriture de l'historique

```bash
git rebase <branche_base>          # Réapplique les commits de la branche actuelle sur une autre branche
```

Options disponibles :

```bash
git rebase -i HEAD~<n>             # Rebase interactif pour modifier les n derniers commits
git rebase --onto <nouvelle_base> <ancienne_base> <branche> # Déplace une série de commits vers une nouvelle base
git rebase --continue              # Continue un rebase après résolution de conflits
git rebase --abort                 # Annule un rebase en cours
git rebase --skip                  # Ignore le commit actuel et passe au suivant
```

## Git tag

### Gestion des versions et étiquettes

```bash
git tag                            # Liste tous les tags existants
```

Options disponibles :

```bash
git tag <nom_tag>                  # Crée un tag léger sur le commit actuel
git tag -a <nom_tag> -m "message"  # Crée un tag annoté avec un message
git tag -l "pattern"               # Liste les tags correspondant au pattern
git show <nom_tag>                 # Affiche les informations sur un tag spécifique
```

### Partager et gérer les tags

```bash
git push origin <nom_tag>          # Envoie un tag spécifique vers le dépôt distant
```

Options disponibles :

```bash
git push origin --tags             # Envoie tous les tags vers le dépôt distant
git tag -d <nom_tag>               # Supprime un tag local
git push origin :refs/tags/<nom_tag> # Supprime un tag distant
git checkout <nom_tag>             # Se positionne sur l'état du code au moment du tag
```

## 📝 Notes d'utilisation

### Format des commandes

- < > : paramètre à remplacer par une valeur
- { } : indique un numéro ou un identifiant

### Bonnes pratiques

- Utilisez `git stash` pour mettre de côté des modifications temporaires sans créer de commit
- Préférez `git rebase -i` pour nettoyer votre historique avant de partager vos changements
- Créez des tags pour marquer les versions importantes du projet
- Utilisez `git bisect` pour trouver rapidement à quel commit un bug a été introduit
- Appliquez `git cherry-pick` avec parcimonie et préférez les merges ou rebases quand c'est possible

### Points de vigilance

- Ne réécrivez jamais l'historique des branches partagées avec `git rebase`
- Faites attention avec `git cherry-pick` qui peut créer des doublons de commits
- N'utilisez pas `git push --force` après avoir modifié des tags
- Vérifiez toujours l'état de votre dépôt avant d'utiliser des commandes destructives
