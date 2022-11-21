---
title: "Évaluation du logiciel Orange Data Mining"
author: "Roch Delannay"
date: "2022-11-21"
categories: [journal]
---

Brouillon de l'évaluation du logiciel Orange Data Mining.

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

## Évaluation du logiciel Orange Data Mining

### Référence

Demsar J, Curk T, Erjavec A, Gorup C, Hocevar T, Milutinovic M, Mozina M, Polajnar M, Toplak M, Staric A, Stajdohar M, Umek L, Zagar L, Zbontar J, Zitnik M, Zupan B (2013) Orange: Data Mining Toolbox in Python, Journal of Machine Learning Research 14(Aug): 2349−2353.

### Description

- Type de logiciel : libre, développé par le laboratoire de bioinformatique (faculté des sciences de l'information et informatique) de l'Université de Llubljana en Slovénie.
- Type de license : Le logiciel est sous GNU General Public License 3.0, les documentation et documents additionnels sont tous sous licence Creative Commons Attribution-ShareAlike.
- Coût : gratuit
- Langage de programmation : Python3 et C++

### Maturité du logiciel

- Âge du logiciel : La version 3 du logiciel remonte à 2013, avec une première _release_ en 2014 (version 3.1). Orange est développé au tout début de l'essor des algorithmes d'intelligence artificielle et dans le même laps de temps que d'autres librairie (python) telle que ScikitLearn.
- Année en affaires de l'entreprise : Le logiciel a été créé et est maintenu par le même laboratoire depuis 2013.
- Le [dépôt Git d'Orange](https://github.com/biolab/orange3) est très dense. Les derniers _commits_ remontent tout juste à quelques heures avant l'écriture de ce billet (21 novembre 2022, 18h00). Ce projet comptabilise à son actif pas moins de 14,442 _commits_, 3800 étoiles, 881 _forks_, plus de 35 _releases_ (la dernière datant du 11 octobre 2022, Release 3.33.0) et pas moins de 92 contributeurs. Un autre éléments démontre l'activité de ce projet est le nombre d'_issues_ (de problèmes ou questions à résoudre) : nous en observons 91 ouvertes et 2017 fermées.

### Interopérabilité

- Compatibilité avec les plateformes et les systèmes d'exploitation : Ce logiciel est compatible avec les systèmes d'exploitation les plus répandus. Nous avons testé de l'installer sous deux OS (Windows 10 et Ubuntu 20.04.5LTS) et nous n'avons rencontré aucune difficulté. Dans le premier cas il s'agit de télécharger un fichier exécutable (`.exe`) et de le lancer, le programme s'occupe du reste. Du côté d'Ubuntu l'installation est encore plus simple : elle est réalisable via l'installateur de paquet Python `pip` ou `Anaconda`, nous avons choisi la première option : tout s'est déroulé sans le moindre bug.