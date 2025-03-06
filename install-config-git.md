# 📥 Git - Installation et Configuration

## 📑 Table des matières
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Configuration](#configuration)
- [Vérification](#vérification)
- [Résolution des problèmes](#résolution-des-problèmes)

## ⚡ Prérequis

### Configuration système requise

#### Windows
- Windows 7 ou version ultérieure (64 bits)
- 2 GB RAM minimum
- 190 MB d'espace disque
- Droits administrateur Windows

#### macOS
- macOS 10.13 (High Sierra) ou version ultérieure
- 2 GB RAM minimum
- 190 MB d'espace disque
- Accès Terminal avec droits sudo

#### Linux
- Toute distribution Linux moderne
- 2 GB RAM minimum
- 190 MB d'espace disque
- Accès Terminal avec droits sudo

### Préparation

#### Windows
```bash
# Aucune préparation spécifique requise
```

#### macOS
```bash
# Installation des Command Line Tools si non présents
xcode-select --install
```

#### Linux
```bash
# Mise à jour des dépôts
sudo apt update        # Pour Debian/Ubuntu/Linux Mint
sudo dnf check-update # Pour Fedora
```

## 💿 Installation

### Windows - Installation via l'installateur
```bash
# Télécharger l'installateur depuis https://git-scm.com/download/win
# Exécuter le fichier .exe téléchargé
```

### macOS - Installation via Homebrew
```bash
# Installation via Homebrew
brew install git

# Alternative via MacPorts
sudo port install git
```

### Linux - Installation via gestionnaire de paquets

#### Debian/Ubuntu
```bash
sudo apt install git-all
```

#### Fedora
```bash
sudo dnf install git-all
```

#### Arch Linux
```bash
sudo pacman -S git
```

#### Linux Mint
```bash

sudo apt install git-all
```

## ⚙️ Configuration

### Configuration de base
```bash
# Configurer nom d'utilisateur
git config --global user.name "Votre Nom"

# Configurer email
git config --global user.email "votre@email.com"

# Configurer l'éditeur par défaut
git config --global core.editor "nano"  # ou vim, code, etc.
```

### Configuration avancée
```bash
# Configurer les couleurs
git config --global color.ui auto

# Configurer le comportement des fins de ligne
git config --global core.autocrlf true  # Pour Windows
git config --global core.autocrlf input # Pour macOS/Linux

# Configurer l'outil de merge
git config --global merge.tool vimdiff
```

### Fichiers de configuration importants
| Fichier | Emplacement | Description |
|---------|-------------|-------------|
| .gitconfig | ~/.gitconfig (Unix) ou C:\Users\<User>\.gitconfig (Windows) | Configuration globale de Git |
| .gitignore | À la racine du projet | Liste des fichiers à ignorer |
| .git/config | Dans chaque dépôt | Configuration spécifique au dépôt |

## ✅ Vérification

### Test de l'installation
```bash
# Vérifier la version installée
git --version

# Vérifier la configuration
git config --list
```

### Résultat attendu
```bash
# Exemple de sortie pour git --version
git version 2.39.2

# Exemple de sortie pour git config --list
user.name=Votre Nom
user.email=votre@email.com
core.editor=nano
color.ui=auto
```

## ❌ Résolution des problèmes

### Problèmes courants

#### Erreur "git n'est pas reconnu comme commande interne" (Windows)
**Symptôme :** La commande git n'est pas reconnue dans le terminal
**Solution :**
```bash
# Réinstaller Git en cochant l'option "Git from the command line and also from 3rd-party software"
# Ou ajouter manuellement Git au PATH système
```

#### Erreur de certificat SSL
**Symptôme :** Erreur SSL certificate problem
**Solution :**
```bash
git config --global http.sslVerify false  # À utiliser avec précaution
```

#### Erreur d'authentification
**Symptôme :** Permission denied (publickey)
**Solution :**
```bash
# Vérifier la clé SSH
ssh -T git@github.com

# Générer une nouvelle clé si nécessaire
ssh-keygen -t rsa -b 4096 -C "votre@email.com"
```

## 📚 Ressources supplémentaires

### Documentation officielle
- [Documentation Git](https://git-scm.com/doc)
- [Git Book](https://git-scm.com/book/fr/v2)
- [Git Reference](https://git-scm.com/docs)

### Communauté
- [Forum Git](https://git-scm.com/community)
- [Stack Overflow - Git](https://stackoverflow.com/questions/tagged/git)
- [GitHub Community](https://github.community/)

---
*Dernière mise à jour : 6 mars 2024*

