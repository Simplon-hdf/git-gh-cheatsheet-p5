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