# GitHub CLI - Installation et Configuration

## Table des matières
- [Prérequis](#prérequis)
- [Installation](#installation)
- [Configuration](#configuration)
- [Vérification](#vérification)
- [Résolution des problèmes](#résolution-des-problèmes)
- [Pour aller plus loin](#pour-aller-plus-loin)

## Prérequis
### 💻 Configuration système requise
- Version OS : Windows 10+, macOS 10.15+, ou Linux
- Espace disque : Minimum 100 MB
- Dépendances : Git doit être installé sur votre système

### 🔧 Préparation
```bash
# Vérifier si Git est installé
git --version
# Si Git n'est pas installé, installez-le d'abord :
# Pour Windows : Téléchargez depuis https://git-scm.com/download/win
# Pour macOS : brew install git
# Pour Ubuntu/Debian : sudo apt-get install git
```

## Installation
### 📥 Instructions par système
```bash
# Pour Windows (via PowerShell)
winget install GitHub.cli
# Pour macOS
brew install gh
# Pour Ubuntu/Debian
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo gpg --dearmor -o /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
# Pour Arch Linux
sudo pacman -S github-cli
# Pour Fedora
sudo dnf install gh
```

## Configuration
### 🔐 Configuration de base
```bash
# Authentification avec GitHub
gh auth login
# Suivez les instructions interactives pour :
# 1. Choisir GitHub.com
# 2. Choisir SSH
# 3. S'authentifier avec le navigateur
```

### ⚙️ Configuration avancée
```bash
# Configurer l'éditeur par défaut
gh config set editor "code" # Pour VS Code
# Configurer le protocole préféré
gh config set git_protocol SSH
```

### 📁 Fichiers de configuration importants
| Fichier | Emplacement | Description |
| ---------- | ------------------------------------------------------------------------------- | ------------------------ |
| config.yml | `~/.config/gh/config.yml` (Unix) ou `%APPDATA%\GitHub CLI\config.yml` (Windows) | Configuration principale |
| hosts.yml | `~/.config/gh/hosts.yml` (Unix) ou `%APPDATA%\GitHub CLI\hosts.yml` (Windows) | Authentification |

## Vérification
### ✅ Test de l'installation
```bash
# Vérifier la version installée
gh --version
# Vérifier le statut de l'authentification
gh auth status
```

### 📋 Résultat attendu
```bash
# Pour gh --version
gh version 2.45.0 (DATE)
# Pour gh auth status
Logged in to github.com as VotreUsername
```

## Résolution des problèmes
### ⚠️ Problèmes courants
#### 🚫 Erreur d'authentification
**Symptôme :** "error logging into github.com: authentication failed"
**Solution :**
```bash
# Réinitialiser l'authentification
gh auth logout
gh auth login
```

#### 🌐 Problème de proxy
**Symptôme :** "dial tcp: lookup api.github.com: no such host"
**Solution :**
```bash
# Configurer le proxy
export HTTPS_PROXY=http://proxy.example.com:8080
export HTTP_PROXY=http://proxy.example.com:8080
```

## Pour aller plus loin
### 📚 Documentation officielle
- [Documentation GitHub CLI](https://cli.github.com/manual/)
- [Guide de démarrage rapide](https://docs.github.com/en/github-cli/github-cli/quickstart)
- [FAQ GitHub CLI](https://cli.github.com/manual/gh_help_reference)

### 👥 Communauté
- [GitHub Community Forum](https://github.community/)
- [Stack Overflow [github-cli]](https://stackoverflow.com/questions/tagged/github-cli)
- [GitHub Discussions](https://github.com/cli/cli/discussions)

---
*Dernière mise à jour : 7 mars 2025*