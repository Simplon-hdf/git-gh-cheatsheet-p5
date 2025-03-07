# Contributing

### Rédaction des fiches markdown sur les commandes Git et GitHub

Lorsque vous ajoutez une nouvelle fiche Markdown sur une commande Git ou GitHub, utilisez les templates disponibles dans le dossier templates afin de garantir une structure uniforme et une présentation cohérente des informations.

Des exemples de fiches sont disponibles dans ce dossier template pour vous aider.

### Convention de nommage des commits

Afin de maintenir une bonne lisibilité et une traçabilité des changements, veuillez suivre la convention suivante pour vos messages de commit :

1. **Structure des messages** :
   - Le message de commit doit commencer par un verbe à l'infinitif (par exemple, "Ajouter", "Corriger", "Mettre à jour", etc.).
   - Utilisez un titre concis de 50 caractères maximum, suivi d'une ligne vide et d'un corps de message détaillant le changement, si nécessaire.

2. **Types de commits** :
   Pour mieux comprendre la nature du commit, utilisez un préfixe indiquant le type de modification. Exemple :

   - `feat()` pour une nouvelle fonctionnalité.
   - `fix()` pour une correction de bug.
   - `docs()` pour des changements dans la documentation.
   - `style()` pour des modifications de style (formatage, espacement, etc.).
   - `refactor()` pour un refactoring de code.
   - `test()` pour les modifications relatives aux tests.
   - `chore()` pour des tâches diverses qui ne modifient pas le code (ex. : mise à jour de dépendances).

   **Exemples** :
   - `feat(Ajouter la section sur les commandes de base Git)`
   - `fix(Corriger une faute d'orthographe dans la section Git clone)`
   - `docs(Mettre à jour les exemples de commandes Git push)`
   - `style(Améliorer la mise en page du fichier README)`
   - `refactor(Organiser les sections du cheat sheet par thème)`
   - `chore(Ajouter un template pour les nouvelles fiches Git)`
   - `docs(Ajouter une section sur l'utilisation de GitHub CLI)`
   - `fix(Corriger l'exemple de fusion dans la section Git merge)`

3. **Rédiger les messages en anglais** :
   Tous les messages de commit doivent être obligatoirement rédigés en anglais pour maintenir la cohérence du projet, y compris les noms de branches et les descriptions dans les PR.

4. **Non-respect des conventions de nommage et des templates** :
   Les commits qui ne respectent pas la convention de nommage des messages ou qui ne suivent pas le template pour la rédaction des fiches markdown seront **rejetés**. Il est essentiel que vos messages de commit soient clairs et descriptifs, et que les fiches markdown soient rédigées selon le format indiqué. Avant de soumettre un commit, assurez-vous qu'il respecte bien ces règles.
