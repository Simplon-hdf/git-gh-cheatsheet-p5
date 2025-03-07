# 🛠 Git - Guide des Commandes pour Dépôts Distants

## 📑 Table des matières
- [Concepts Fondamentaux](#concepts-fondamentaux)
- [Gestion du Dépôt Distant](#gestion-du-dépôt-distant)
- [Synchronisation](#synchronisation)
- [Collaboration](#collaboration)
- [Notes d'utilisation](#notes-dutilisation)

## 🎓 Concepts Fondamentaux

### Dépôt Local (Local Repository)
Un dépôt local est une copie du projet sur votre machine. Il contient :
- Le code source du projet
- L'historique complet des modifications (commits)
- Les branches locales
- Un dossier `.git` qui gère toutes ces informations

### Dépôt Distant (Remote Repository)
Un dépôt distant est une version du projet hébergée sur un serveur (comme GitHub, GitLab, Bitbucket) qui permet :
- Le partage du code entre développeurs
- La sauvegarde du projet
- La collaboration en équipe

Le dépôt distant le plus couramment utilisé est nommé "origin".

### Fork
Un fork est une copie personnelle d'un dépôt distant d'un autre utilisateur. Il permet de :
- Travailler sur sa propre version du projet
- Proposer des modifications au projet original via des Pull Requests
- Expérimenter sans affecter le projet original

Le fork crée un nouveau dépôt distant sous votre compte.

### Upstream
L'upstream désigne le dépôt distant original à partir duquel vous avez créé votre fork. Il est important car il permet de :
- Synchroniser votre fork avec les dernières modifications du projet original
- Récupérer les mises à jour du projet source
- Maintenir votre fork à jour

### Workflow Typique
1. Fork du projet original sur GitHub
2. Clone de votre fork en local
3. Ajout de l'upstream pour suivre le projet original
4. Développement sur votre fork
5. Synchronisation régulière avec l'upstream
6. Proposition de modifications via Pull Request

## 🌐 Gestion du Dépôt Distant

### 🔗 Connexion aux Dépôts Distants

Lorsque vous travaillez avec Git, il existe trois principales manières de se connecter à un dépôt distant, chacune adaptée à un cas d'usage spécifique :

1. **Démarrer avec un projet existant (Clone)**
   - Utilisez `git clone` quand vous voulez commencer à travailler sur un projet existant
   - Cette commande :
     - Crée une copie complète du dépôt distant
     - Configure automatiquement "origin" comme dépôt distant
     - Télécharge tout l'historique et les branches
     - Crée la connexion avec le dépôt distant

2. **Publier un projet local (Origin)**
   - Utilisez `git remote add origin` quand vous avez déjà un projet local que vous voulez publier
   - Cette commande :
     - Connecte votre projet local à un dépôt distant vide
     - Nomme ce dépôt "origin" par convention
     - Ne télécharge aucun code (car le dépôt distant est vide)
     - Prépare la publication de votre code

3. **Contribuer à un projet forké (Upstream)**
   - Utilisez `git remote add upstream` après avoir forké un projet
   - Cette commande :
     - Ajoute une connexion vers le dépôt source original
     - Permet de rester synchronisé avec le projet original
     - S'utilise en complément de "origin" qui pointe vers votre fork
     - Facilite la récupération des mises à jour

### Commandes de Configuration

#### Configuration de l'Upstream
```bash
git remote add upstream [url-repo-original]         # Ajouter le dépôt source comme upstream
```
Options disponibles :
```bash
git fetch upstream                                 # Récupérer les modifications de l'upstream
git merge upstream/[branche]                       # Fusionner les modifications de l'upstream
git pull upstream [branche]                        # Récupérer et fusionner depuis l'upstream
```


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
Options disponibles :
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
- Synchroniser régulièrement avec l'upstream pour éviter les conflits majeurs
- Vérifier l'état de votre fork avant de créer une Pull Request

### ⚠️ Points de vigilance
- Ne jamais push --force sur main/master
- Toujours vérifier la branche active avant un push
- Résoudre les conflits localement avant de push
- S'assurer que votre fork est à jour avant de créer une Pull Request
- Bien configurer l'upstream pour maintenir la synchronisation

## 📚 Pour aller plus loin

### Documentation Officielle
- [Git Remote Documentation](https://git-scm.com/docs/git-remote) - Documentation officielle sur les dépôts distants
- [Git Book - Working with Remotes](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Travailler-avec-des-d%C3%A9p%C3%B4ts-distants) - Chapitre sur les dépôts distants en français
- [GitHub Docs](https://docs.github.com/fr) - Documentation GitHub en français

