## [Commande de base]

### [git init]
```bash
[git init]              # [Crée ou réinitialise un dépôt Git]
```

Options disponibles :
```bash
[git init] [--bare]              # [Crée un dépot Git sans working directory]
[git init] [--quiet]              # [Affiche seulement les messages d'erreur.]
[git init] [-b] <nom de la branche>             # [Choisir le nom de la première branche]
```

### [git add]
```bash
[git add]              # [Ajoute un ou plusieurs fichier(s) dans la zone de staging.]
```

Options disponibles :
```bash
[git add] ["nom du fichier 1"] <"nom du fichier 2">              # [Ajoute les fichiers en options]
[git add] [*]              # [Ajoute tous les fichiers non cachés]
[git add] [.]              # [Ajoute tous les fichiers]
```

### [git commit]
```bash
[git commit]              # [Crée un nouveau commit]
```

Options disponibles :
```bash
[git commit] [-m] <"message">              # [Ajoute un message au commit]
[git commit] [-am] <"message">              # [Ajoute à la zone de staging et commit tous les fichiers qui ont des changements]
[git commit] [-amend] [-m] <"message">            # [Permet de modifier le dernier commit]
[git commit] [-amend] [--no-edit]            # [modifier sans changer le message]
```