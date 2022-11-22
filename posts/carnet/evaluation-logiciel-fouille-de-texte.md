---
title: "Évaluation du logiciel Orange Data Mining"
author: "Roch Delannay"
date: "2022-11-21"
categories: [journal]
---
::: {.content-hidden when-format="pdf"}

Brouillon de l'évaluation du logiciel Orange Data Mining.

![](images-orange/image-orange.png)

## Rappel des critères

### Description

- Type de logiciel (libre, propriétaire, etc.)
- Type de licence (fixe, libre, académique, mixte, etc.)
- Coût
- Langage de programmation (Python, Java, etc.)

### Maturité du logiciel

- Âge du logiciel
- Année en affaires de l'entreprise
- Nombre de mois depuis la dernière mise à jour
- Le logiciel est-il encore supporté par le développeur ou le créateur

### Interopérabilité

Critères qui impliquent la capacité du logiciel à s'harmoniser avec le système déjà en place et sa faculté de fonctionner conjointement avec d'autres ressources logicielles et matérielles.

- Compatibilité avec les plateformes et systèmes d'exploitation
- Intégration Web
- Intégration à d'autres applications
- Dépendances logicielles ou matérielles

### Soutien technique

Critères qui mesurent l'aide disponible pour les utilisateurs du logiciel.

- Accès à une version de démonstration
- Assistance technique
- Documentation 
- Tutoriel
- Communauté

:::
## Évaluation du logiciel Orange Data Mining
### Description

- Type de logiciel : *Orange Data Mining* (Orange) est un logiciel libre, développé par le laboratoire de bioinformatique (faculté des sciences de l'information et informatique) de l'Université de Llubljana en Slovénie.
- Type de licence : Le logiciel est sous GNU General Public License 3.0, les documentations et documents additionnels sont tous sous licence Creative Commons Attribution-ShareAlike.
- Coût : Aucun paiement n'est requis pour utiliser le logiciel, toutefois il est possible d'effectuer une donation pour financer le projet.
- Langage de programmation : La base logicielle est développée en C++, et les *widgets*, nous y reviendrons plus tard, sont développés avec le langage de programmation Python.

### Maturité du logiciel

- Âge du logiciel : La version 3 du logiciel remonte à 2013, avec une première _release_ en 2014 (version 3.1). Orange est développé au tout début de l'essor des algorithmes d'intelligence artificielle et dans le même laps de temps que d'autres librairies (python) telle que ScikitLearn.
- Année en affaires de l'entreprise : Le logiciel a été créé et est maintenu par le même laboratoire depuis 2013.
- Le [dépôt Git d'Orange](https://github.com/biolab/orange3) est très dense. Les derniers _commits_ remontent tout juste à quelques heures avant l'écriture de ce billet (21 novembre 2022, 18h00). Ce projet comptabilise à son actif pas moins de 14,442 _commits_, 3800 étoiles, 881 _forks_, plus de 35 _releases_ (la dernière datant du 11 octobre 2022, Release 3.33.0) et pas moins de 92 contributeurs. Un autre élément démontre l'activité de ce projet est le nombre d'_issues_ (de problèmes ou questions à résoudre) : nous en observons 91 ouvertes et 2017 fermées.

### Interopérabilité

- Compatibilité avec les plateformes et les systèmes d'exploitation : Ce logiciel est compatible avec les systèmes d'exploitation les plus répandus. Nous avons testé de l'installer sous deux OS (Windows 10 et Ubuntu 20.04.5 LTS) et nous n'avons rencontré aucune difficulté. Dans le premier cas, il s'agit de télécharger un fichier exécutable `.exe` et de l'exécuter, le *wizard* d'installation s'occupe alors du reste. Du côté d'Ubuntu l'installation est encore plus simple : elle est réalisable dans le terminal via l'installateur de paquet Python `pip` ou `Anaconda`, nous avons choisi la première option : tout s'est déroulé sans le moindre bug.

- Intégration à d'autres applications : Orange n'est pas forcément prévu pour s'inscrire dans un écosystème où les logiciels peuvent communiquer entre eux. Les formats de données utilisables en entrée du processus sont assez larges tant qu'ils respectent la forme d'un tableau (`.xlsx`, `.csv`, Google Sheet, table d'une base de données SQL). Par contre, l'export est plus mince : seules les visualisations générées et les modèles (*workflows*) peuvent être exportés depuis le logiciel. Cependant, le logiciel offre beaucoup de plasticité, notamment au niveau des méthodes mises en œuvre puisqu'il est possible de développer ses propres *widgets* en Python et de les utiliser dans Orange, par exemple pour créer des workflows adaptés à des questions de recherche ou des modèles de données peu conventionnels.
- Dépendances logicielles ou matérielles : Il n'y aucune dépendance hormis le langage de programmation Python (qui est nativement installé sur les Mac et les Linus).

### Soutien technique

Critères qui mesurent l'aide disponible pour les utilisateurs du logiciel.

- Accès à une version de démonstration : Il n'y a pas réellement de version de démonstration. Plusieurs exemples sont fournis à l'intérieur du logiciel et permettent de tester directement différents *workflows* ou méthodes à appliquer à des corpus de données. D'ailleurs, plusieurs corpus sont également disponibles avec le logiciel. Au-delà de leur emploi et de l'application de calculs sur ces données, il est possible de les ouvrir et regarder la structure des données (fait sans doute important lors d'une phase d'apprentissage des outils d'intelligence artificielle).
- Assistance technique : Il est possible de prendre contact avec la communauté Orange à travers différentes plateformes : le site Web, les réseaux sociaux, ou encore Discord et Stack Exchange.
- Documentation : Orange fournit des documentations très précises quant aux différents usages du logiciel ou des développements possibles. Cependant, nous noterons que la documentation ne décrit pas complètement le comportement des algorithmes que les usagers vont employer.
- Tutoriels : Des tutoriels et des exemples sont disponibles un peu partout dans Orange : il est possible de trouver dans le logiciel des *workflows* génériques et prêt à l'emploi, avec des explications pour chacune des étapes à réaliser. L'équipe d'orange a également publié des tutoriels vidéos sur la plateforme Youtube et des documentations plus poussées pour des utilisateurs avancés. En tant que nouvel utilisateur, nous nous sentons vraiment accompagné dans l'apprentissage de l'outil.

### Quelques essais de l'outil

## Références

- Demsar J, Curk T, Erjavec A, Gorup C, Hocevar T, Milutinovic M, Mozina M, Polajnar M, Toplak M, Staric A, Stajdohar M, Umek L, Zagar L, Zbontar J, Zitnik M, Zupan B (2013) Orange: Data Mining Toolbox in Python, Journal of Machine Learning Research 14(Aug): 2349−2353.

- Site Web du logiciel : https://orangedatamining.com/
- Documentation Data Mining Library : https://orange3.readthedocs.io/projects/orange-data-mining-library/en/latest/index.html#
- Documentation utilisateurs (visual programming) : https://orange3.readthedocs.io/projects/orange-visual-programming/en/latest/index.html
- Documentation développements : https://orange3.readthedocs.io/projects/orange-development/en/latest/index.html
- GitHub du projet : https://github.com/biolab/orange3

