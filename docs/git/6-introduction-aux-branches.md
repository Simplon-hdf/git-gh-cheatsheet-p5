# Git - Commandes Avancées

## Table des matières
- [Git Stash](#git-stash)
- [Git Diff](#git-diff)
- [Git Bisect](#git-bisect)
- [Git Blame](#git-blame)
- [Git Grep](#git-grep)
- [Git Cherry-Pick](#git-cherry-pick)
- [Git Rebase](#git-rebase)
- [Git Tag](#git-tag)
- [Notes d'utilisation](#notes-dutilisation)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Git Stash

### 📦 Sauvegarder des modifications temporaires
```bash
git stash                          # Stocke les modifications locales dans une réserve temporaire
```

Options disponibles :
```bash
git stash save "message"           # Stocke les modifications avec un message descriptif
git stash -p                       # Mode interactif pour choisir quels changements stocker
git stash --include-untracked      # Inclut également les fichiers non suivis
```

### 📋 Gérer les stashs
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

## Git Diff

### 🔍 Analyser les différences
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

## Git Bisect

### 🔎 Déboguer avec la recherche binaire
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

## Git Blame

### 👤 Savoir qui a écrit chaque ligne
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

## Git Grep

### 🔍 Trouver un mot ou une phrase
```bash
git grep [motif]                   # Recherche un motif dans les fichiers
```

Options disponibles :
```bash
git grep -i [motif]                # Recherche sans tenir compte de la casse
git grep -l [motif]                # Affiche seulement les noms de fichiers contenant le motif
git grep -n [motif]                # Affiche les lignes et numéros de ligne où le motif est trouvé
git grep -v [motif]                # Exclut les lignes contenant le motif et les affiche
git grep -w [motif]                # Recherche le motif en tant que mot entier
git grep -e [motif]                # Permet de chercher un motif qui commence par "-"
```

## Git Cherry-Pick

### 🍒 Appliquer des commits spécifiques
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

## Git Rebase

### 🔄 Réécriture de l'historique
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

## Git Tag

### 🏷️ Gestion des versions et étiquettes
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

### 📤 Partager et gérer les tags
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

## Notes d'utilisation

### ⌨️ Format des commandes
- [paramètre] : paramètre obligatoire
- <paramètre> : paramètre optionnel
- {n} : indique un numéro ou un identifiant

### ✅ Bonnes pratiques
- Utilisez `git stash` pour mettre de côté des modifications temporaires sans créer de commit
- Préférez `git rebase -i` pour nettoyer votre historique avant de partager vos changements
- Créez des tags pour marquer les versions importantes du projet
- Utilisez `git bisect` pour trouver rapidement à quel commit un bug a été introduit
- Appliquez `git cherry-pick` avec parcimonie et préférez les merges ou rebases quand c'est possible

### ⚠️ Points de vigilance
- Ne réécrivez jamais l'historique des branches partagées avec `git rebase`
- Faites attention avec `git cherry-pick` qui peut créer des doublons de commits
- N'utilisez pas `git push --force` après avoir modifié des tags
- Vérifiez toujours l'état de votre dépôt avant d'utiliser des commandes destructives

## Pour aller plus loin

### 📚 Documentation officielle
- [git stash](https://git-scm.com/docs/git-stash) - Documentation complète de git stash
- [git diff](https://git-scm.com/docs/git-diff) - Documentation complète de git diff
- [git bisect](https://git-scm.com/docs/git-bisect) - Documentation complète de git bisect
- [git blame](https://git-scm.com/docs/git-blame) - Documentation complète de git blame
- [git grep](https://git-scm.com/docs/git-grep) - Documentation complète de git grep
- [git cherry-pick](https://git-scm.com/docs/git-cherry-pick) - Documentation complète de git cherry-pick
- [git rebase](https://git-scm.com/docs/git-rebase) - Documentation complète de git rebase
- [git tag](https://git-scm.com/docs/git-tag) - Documentation complète de git tag

### 🎓 Ressources d'apprentissage
- [Git Book - Commandes avancées](https://git-scm.com/book/fr/v2) - Chapitre sur les commandes avancées
- [Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials) - Tutoriels détaillés sur Git
- [Git Explorer](https://gitexplorer.com/) - Outil interactif pour explorer les commandes Git