# Git - Guide des Commandes

## Table des matières
- [Commande de retour en arrière](#commande-de-retour-en-arrière)
- [Notes d'utilisation](#notes-dutilisation)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Commande de retour en arrière

### ↩️ git reset
```bash
git reset # Renvoie la HEAD à un précédent commit
```

Options disponibles :
```bash
git reset [--soft HEAD~X] # Annule les X derniers commits en gardant les modifications dans la zone de staging
git reset [--mixed HEAD~X] # Annule les X derniers commits et retire les modifications dans la zone de staging
git reset [--hard HEAD~X] # Annule les X derniers commits et supprime définitivement les modifications du working directory
git reset [commit hash] # Retourne la HEAD au commit
git reset [--hard] [commit hash] # Retourne la HEAD au commit et supprime les modifications
git reset [--keep] [commit hash] # Retourne la HEAD au commit et garde les modifications
```

### 🔄 git revert
```bash
git revert # Crée un commit qui annule les modifications du commit spécifié
```

Options disponibles :
```bash
git revert [HEAD] # Annule le dernier commit en créant un nouveau commit
git revert [commit hash] # Annule le commit spécifié en créant un nouveau commit
git revert [-n] [commit hash] # Annule le commit spécifié sans créer un nouveau commit
git revert [-m] [1] | [2] # Annule le merge et revient à l'état du parent choisi en créant un nouveau commit.
git revert [--continue] # Continue un revert qui cause un conflit
git revert [--abort] # Annule un revert qui cause un conflit
```

## Notes d'utilisation

### ⌨️ Format des commandes
- [paramètre] : paramètre obligatoire
- | : choix entre plusieurs options

### ✅ Bonnes pratiques
- Privilégier git reset --soft pour garder les modifications au cas où.
- Utiliser git status avant git reset --hard.
- Utiliser git revert au lieu de git reset pour annuler un commit en conservant l'historique.

### ⚠️ Points de vigilance
- git reset --hard supprime définitivement les modifications locales, il est irréversible sans sauvegarde
- Un revert ne supprime pas un commit, il crée un nouveau commit, ce qui peut compliquer l'historique.

## Pour aller plus loin

### 📚 Documentation officielle
- [git reset](https://git-scm.com/docs/git-reset) - Documentation complète de git reset
- [git revert](https://git-scm.com/docs/git-revert) - Documentation complète de git revert

### 🎓 Ressources d'apprentissage
- [Git Book - Annulation de commits](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Annuler-des-actions) - Chapitre sur l'annulation de commits
- [Git Explorer - Reset & Revert](https://gitexplorer.com/) - Guide interactif pour les commandes reset et revert
- [Atlassian Git Tutorial - Reset, Checkout, et Revert](https://www.atlassian.com/git/tutorials/resetting-checking-out-and-reverting) - Guide détaillé sur les différences entre reset, checkout et revert