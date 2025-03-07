# 🛠 Git - Guide des Branches

## Introduction aux branches

### Concept de branche
```bash
git branch                          # Affiche toutes les branches locales
```

Git permet de gérer les branches pour travailler sur plusieurs fonctionnalités ou correctifs en parallèle. Chaque branche est un environnement indépendant où les développeurs peuvent effectuer des modifications sans perturber le travail des autres. La branche principale est souvent appelée main ou master, mais des branches spécifiques peuvent être créées pour développer de nouvelles fonctionnalités, corriger des bugs ou expérimenter.

## Créer et basculer entre les branches

### Création d'une branche
```bash
git branch <nom_branche>           # Crée une nouvelle branche sans y basculer
```

Options disponibles :
```bash
git branch -v                      # Affiche les branches locales avec le dernier commit sur chaque branche
git branch --merged                # Affiche les branches qui ont été fusionnées dans la branche courante
git branch --no-merged             # Affiche les branches qui n'ont pas été fusionnées dans la branche courante
```

### Basculer entre branches
```bash
git checkout <nom_branche>         # Change la branche courante pour nom_branche
```

Options disponibles :
```bash
git checkout -b <nom_branche>      # Crée une nouvelle branche nommée nom_branche et se déplace dessus
git switch <nom_branche>           # Change la branche courante pour nom_branche (équivalent à git checkout <nom_branche>)
git switch -c <nom_branche>        # Crée une nouvelle branche nommée nom_branche et se déplace dessus (équivalent à git checkout -b <nom_branche>)
```