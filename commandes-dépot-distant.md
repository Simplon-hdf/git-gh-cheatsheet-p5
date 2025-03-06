# 🛠 Git - Guide des Commandes pour Dépôts Distants

## 📑 Table des matières
- [Gestion du Dépôt Distant](#gestion-du-dépôt-distant)
- [Synchronisation](#synchronisation)
- [Collaboration](#collaboration)
- [Notes d'utilisation](#notes-dutilisation)

## Gestion du Dépôt Distant
### Connexion au Dépôt
```bash
git remote add origin [url]                        # Lier un dépôt distant
```
Options disponibles :
```bash
git remote -v                                      # Afficher les dépôts distants liés
git remote remove [nom]                           # Supprimer un dépôt distant
git remote rename [ancien] [nouveau]              # Renommer un dépôt distant
```

### Clonage et Configuration
```bash
git clone [url]                                    # Cloner un dépôt distant
```
Options disponibles :
```bash
git clone --branch [branche] [url]                # Cloner une branche spécifique
git clone --depth 1 [url]                         # Cloner uniquement le dernier commit
git clone [url] [dossier]                         # Cloner dans un dossier spécifique
```

## Synchronisation
### Envoi des Modifications
```bash
git push origin [branche]                          # Envoyer les commits vers le dépôt distant
```
Options disponibles :
```bash
git push -u origin [branche]                      # Premier push d'une nouvelle branche
git push --force-with-lease                       # Forcer le push (avec vérification)
git push --tags                                   # Envoyer les tags
```

### Récupération des Modifications
```bash
git pull origin [branche]                          # Récupérer et fusionner les modifications
```
Options disponibles :
```bash
git fetch origin                                  # Récupérer sans fusionner
git fetch --all                                   # Récupérer depuis tous les dépôts distants
git pull --rebase origin [branche]               # Récupérer en réappliquant les commits locaux
```

## Collaboration
### Gestion des Branches Distantes
```bash
git branch -r                                      # Lister les branches distantes
```
Options disponibles :
```bash
git checkout -b [locale] origin/[distante]        # Créer une branche locale depuis une distante
git push origin --delete [branche]                # Supprimer une branche distante
git fetch origin --prune                          # Nettoyer les branches supprimées
```

### Suivi des Modifications
```bash
git branch -vv                                     # Voir les branches et leurs tracking
```
Options disponibles :
```bash
git log origin/[branche]..                        # Voir les commits non pushés
git diff origin/[branche]                         # Voir les différences avec le distant
git remote show origin                            # Voir l'état détaillé du dépôt distant
```

## 📝 Notes d'utilisation
### Format des commandes
- [paramètre] : paramètre obligatoire
- <paramètre> : paramètre optionnel

### Bonnes pratiques
- Toujours faire un git fetch avant de commencer à travailler
- Privilégier --force-with-lease à --force pour éviter d'écraser le travail des autres
- Créer des branches locales pour chaque fonctionnalité

### Points de vigilance
- Ne jamais push --force sur main/master
- Toujours vérifier la branche active avant un push
- Résoudre les conflits localement avant de push

---
*Ce guide se concentre sur les commandes Git pour travailler avec des dépôts distants. Pour la configuration locale et les commandes de base, référez-vous à la documentation générale de Git.* 
