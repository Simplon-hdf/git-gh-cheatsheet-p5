# 🛠 Git - Guide des Commandes pour Dépôts Distants

## 📑 Table des matières
- [Gestion du Dépôt Distant](#gestion-du-dépôt-distant)
- [Synchronisation](#synchronisation)
- [Collaboration](#collaboration)
- [Notes d'utilisation](#notes-dutilisation)

## 🌐 Gestion du Dépôt Distant
### Configuration de l'Upstream
```bash
git remote add upstream [url-repo-original]         # Ajouter le dépôt source comme upstream
```
Options disponibles :
```bash
git fetch upstream                                 # Récupérer les modifications de l'upstream
git merge upstream/[branche]                       # Fusionner les modifications de l'upstream
git pull upstream [branche]                        # Récupérer et fusionner depuis l'upstream
```

### 🔗 Connexion au Dépôt
```bash
git remote add origin [url]                        # Lier un dépôt distant
```
Options disponibles :
```bash
git remote -v                                      # Afficher les dépôts distants liés
git remote remove [nom]                           # Supprimer un dépôt distant
git remote rename [ancien] [nouveau]              # Renommer un dépôt distant
```

### 📥 Clonage et Configuration
```bash
git clone [url]                                    # Cloner un dépôt distant
```
Options disponibles :
```bash
git clone --branch [branche] [url]                # Cloner une branche spécifique
git clone --depth 1 [url]                         # Cloner uniquement le dernier commit
git clone [url] [dossier]                         # Cloner dans un dossier spécifique
```

## 🔄 Synchronisation
### 📤 Envoi des Modifications
```bash
git push origin [branche]                          # Envoyer les commits vers le dépôt distant
```
Options disponibles :
```bash
git push -u origin [branche]                      # Premier push d'une nouvelle branche
git push --force-with-lease                       # Forcer le push (avec vérification)
git push --tags                                   # Envoyer les tags
```

### 📥 Récupération des Modifications
```bash
git pull origin [branche]                          # Récupérer et fusionner les modifications
```
Options disponibles
```bash
git fetch origin                                  # Récupérer sans fusionner
git fetch --all                                   # Récupérer depuis tous les dépôts distants
git pull --rebase origin [branche]               # Récupérer en réappliquant les commits locaux
```

## 👥 Collaboration

### 🌿 Gestion des Branches Distantes

```bash
git branch -r                                      # Lister les branches distantes

```

Options disponibles :

```bash
git checkout -b [locale] origin/[distante]        # (Ancienne méthode) Créer une branche locale depuis une distante
git branch [locale] origin/[distante]             # Créer une branche locale depuis une distante
git switch [locale]                              # Basculer sur la nouvelle branche
git push origin --delete [branche]                # Supprimer une branche distante
git fetch origin --prune                          # Nettoyer les branches supprimées

```

### 👀 Suivi des Modifications

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
### ⌨️ Format des commandes
- [paramètre] : paramètre obligatoire
- <paramètre> : paramètre optionnel
- | : choix entre plusieurs options

### ✅ Bonnes pratiques
- Toujours faire un git fetch avant de commencer à travailler
- Privilégier --force-with-lease à --force pour éviter d'écraser le travail des autres
- Créer des branches locales pour chaque fonctionnalité

### ⚠️ Points de vigilance
- Ne jamais push --force sur main/master
- Toujours vérifier la branche active avant un push
- Résoudre les conflits localement avant de push

---

## 📚 Pour aller plus loin

### Documentation Officielle
- [Git Remote Documentation](https://git-scm.com/docs/git-remote) - Documentation officielle sur les dépôts distants
- [Git Book - Working with Remotes](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Travailler-avec-des-d%C3%A9p%C3%B4ts-distants) - Chapitre sur les dépôts distants en français
- [GitHub Docs](https://docs.github.com/fr) - Documentation GitHub en français

### Guides Pratiques
- [Atlassian Git Tutorial - Remote Repositories](https://www.atlassian.com/git/tutorials/syncing) - Guide détaillé sur la synchronisation
- [GitHub Flow](https://docs.github.com/fr/get-started/quickstart/github-flow) - Workflow recommandé par GitHub

*Ce guide se concentre sur les commandes Git pour travailler avec des dépôts distants. Pour approfondir vos connaissances, n'hésitez pas à consulter les ressources ci-dessus.*
