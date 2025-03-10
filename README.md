# Cheat sheet Git et GitHub CLI

## 📝 Description

Ce guide a pour objectif de fournir une vue d'ensemble sur l'utilisation de **Git** et de **GitHub CLI** pour gérer efficacement le code source et collaborer sur des projets. Il s'adresse à la fois aux développeurs novices qui souhaitent s'initier aux principes de base du contrôle de version, ainsi qu'aux utilisateurs plus expérimentés cherchant à maîtriser des outils avancés pour optimiser leur flux de travail et leurs interactions avec GitHub.

<details>
  <summary><img src="https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg" alt="GitHub Logo" width="24" height="24">
 <strong>1. Documentation complète de GitHub CLI</strong></summary>
<br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/gh-cli/1-introduction.md">   2.1 Qu'est-ce que GitHub CLI  </a></li>
<br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/gh-cli/2-pr%C3%A9requis.md">   2.2 Prérequis ainsi qu'installation de GitHub CLI  </a></li>
<br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/gh-cli/3-gestion-des-d%C3%A9p%C3%B4ts.md">   2.3 Gestion des dépôts via GitHub CLI  </a></li>
<br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/gh-cli/4-gestion-des-actions.md">   2.4 Gestion des actions via GitHub CLI  </a></li>
<br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/gh-cli/5-commandes-supplementaire.md">   2.5 Commandes supplementaire de GitHub CLI  </a></li>
<br>
</details>
<br>
<details>
  <summary><img src="https://humancoders-formations.s3.amazonaws.com/uploads/course/logo/10/formation-git.png" alt="Git Logo" width="24" height="24">
<strong>2. Documentation complète de Git</strong></summary>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/1-introduction.md">   2.1 Qu'est-ce que Git  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/2-pr%C3%A9requis.md">   2.2 Prérequis ainsi qu'installation de Git  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/3-commande-de-base.md">   2.3 Les commandes de base  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/4-concepts-fondamentaux.md">   2.3 Les concepts fondamentaux de Git  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/5-commande-de-retour-en-arriere.md">   2.4 Commande de retour en arrière sur Git  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/6-introduction-aux-branches.md">   2.5 Introduction aux branches de Git  </a></li>
  <br>
  <li><a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/docs/git/7-commandes-avanc%C3%A9es.md">   2.6 Commandes avancées de Git  </a></li>
  </ul>
</details>
<br>
<details>
  <summary><strong>❓ But du projet</strong></summary>
<br>
Ce projet a pour objectif de fournir une <strong>vue d'ensemble complète</strong> des outils <strong>Git</strong> et <strong>GitHub CLI</strong>.
Il regroupe les principales commandes et fonctionnalités de <strong>Git</strong> et <strong>GitHub</strong> en un seul endroit,
permettant ainsi de gérer efficacement le code source, de collaborer avec d'autres développeurs et
d'automatiser les interactions avec <strong>GitHub</strong> en ligne de commande.

Ce guide est conçu pour être utilisé aussi bien par les développeurs débutants que par les utilisateurs plus expérimentés,
afin de maîtriser les outils de versionnement et de gestion de projet.

</details>
<br>
<details> 
<summary> <strong>⚙️ Built with</strong></summary>
<br>
<ul>
<li>

<img src="https://camo.githubusercontent.com/7e282220b8ec0dd29cf99be1c0f5e82d74a42bc84ed834ee6afd86b4bad3bfee/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6769746875622d2532333132313031312e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d676974687562266c6f676f436f6c6f723d7768697465"/>

</li>
<li>

<img src="https://camo.githubusercontent.com/836e0b69e70e4620ddeae99dc99913f5ccbc7cfff6e854587f0d9a6512ce996d/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f6d61726b646f776e2d2532333030303030302e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d6d61726b646f776e266c6f676f436f6c6f723d7768697465"/>

</li>
<li>

<img src="https://camo.githubusercontent.com/3e78414c94a71a544ae82fbe7a2e9d6f0863521d15fde32d2c299cabfbcb9c23/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f56697375616c25323053747564696f253230436f64652d3030373864372e7376673f7374796c653d666f722d7468652d6261646765266c6f676f3d76697375616c2d73747564696f2d636f6465266c6f676f436f6c6f723d7768697465"/>

</li>
</ul>
</details>

<br>
<details>
  <summary><strong>🧑‍🔧 Vous voulez contribuer au projet ?</strong></summary>
  <br>
  Vous devez suivre plusieurs étapes pour y participer :
  <br>
  <br>
  La première étape importante est de se référer au guide de contribution disponible <a href="https://github.com/Simplon-hdf/git-gh-cheatsheet-p5/blob/develop/CONTRIBUTING.md">ici</a>.
  <br>
  <br>
  <ul>
    <li><strong>Forkez le dépôt :</strong> Créez une copie du projet sur votre propre compte GitHub.</li>
  </ul>
  <pre><code>https://github.com/Simplon-hdf/git-gh-cheatsheet-p5.git</code></pre>

  <ul>
    <li><strong>Clonez votre fork :</strong> Clonez votre version du projet sur votre machine locale.</li>
  </ul>
  <pre><code>git clone https://github.com/VOTRE_UTILISATEUR/git-gh-cheatsheet-p5.git</code></pre>

  <ul>
    <li><strong>Créez une nouvelle branche à partir de <em>develop</em> :</strong> Avant de commencer à travailler sur une nouvelle fonctionnalité, assurez-vous d'être sur la branche <em>develop</em>.</li>
  </ul>
  <pre><code>git switch develop</code></pre>
  <pre><code>git checkout -b ma-nouvelle-fonctionnalite</code></pre>

  <ul>
    <li><strong>Une fois votre fonctionnalité terminée, effectuez un commit et poussez vos changements :</strong></li>
  </ul>
  <pre><code>git push origin ma-nouvelle-fonctionnalite</code></pre>

  <ul>
    <li><strong>Enfin, ouvrez une pull request vers la branche <em>develop</em> du projet principal :</strong> Nous examinerons votre PR dès que possible ! 📥</li>
  </ul>
</details>

<br>
<details>
  <summary><strong>🧑‍💻 Crédits</strong></summary>
<br>
Merci aux personnes qui ont contribué à ce projet !

  <ul> 
    <li><a href="https://github.com/glerique">Gaël</a></li>
    <li><a href="https://github.com/kenlark">Kenzo</a></li>
    <li><a href="https://github.com/joydfr">Jody</a></li>
    <li><a href="https://github.com/Exizygl">Bastien</a></li>
  </ul>
</details>
