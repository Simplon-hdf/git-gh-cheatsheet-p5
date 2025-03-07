# 🔧 Git - Commandes Avancées

## Git stash

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

## Git diff

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

## Git bisect

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


