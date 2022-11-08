---
title: "Écriture du TP02 part2"
author: "Roch Delannay"
date: "2022-11-08"
categories: [journal]
---

Compte-rendu du TP02 : description du corpus de données.

## Rappel des critères

1. Critères généraux
− Titre
− Auteur(s)
− Date de publication
− Référence complète
− Droits d'auteurs et contraintes juridiques
− Taille (nombre de mots du corpus entier et moyenne approximative du nombre de mots des documents)
2. Critères technologiques
− Provenance
− Support
− Format(s) des documents constituants le corpus
3. Critères Informationnels
− Discipline
− Sujets
− Présentation sommaire du corpus
− Justification du lien entre la tâche à réaliser et le corpus
4. Critères linguistiques
− Genre
− Registre de langue
− Langue
5. Difficultés rencontrées et commentaires
− Veuillez indiquer les difficultés que vous avez rencontrées ou les commentaires que vous jugez pertinents de noter lors de la constitution de votre corpus, le cas échéant.


## Présentation du corpus


## Preprocessing du corpus

### Récupération des données

Mettre le post sur la transformation des données de l'API : JSON to CSV

Ajouter quelques lignes du csv pour l'exemple

Mettre le fichier csv en pièce jointe

### Preprocessing avec [Orange Data Mining](https://orangedatamining.com/)

Le corpus au format `CSV` est brut, nous y trouvons seulement les épigrammes grecques et leur URL pour les identifier, mais nous aurons certainement besoin de le compléter avec d'autres informations et/ou de le réduire pour correspondre au mieux à notre problématique.

![](imagesSCI6203-tp02/csv.png)

![](imagesSCI6203-tp02/preprocessing1.PNG)

Afin de comprendre comment nous allons pouvoir travailler avec cet objet, nous avons décidé d'effectuer des premiers tests de *preprocessing* avec le logiciel _Orange Data Mining_. Orange est un outils de programmation visuelle, l'utilisation de `widgets` dans l'espace de travail du logiciel permet de créer un `workflow` et d'appliquer une suite d'opérations aux données du corpus. Nous avons suivi l'un des workflows proposé en exemple dans la documentation du logiciel afin d'observer la forme des résultats que nous pouvons obtenir. 
Les widgets utilisés sont les suivants : 

- `Preprocess Text` : ce widget permet de transformer (lowercase), de tokeniser (Regex `\w+`), de normaliser (lemmatiser en grec) et de filtrer (liste de *stopwords* créée par l'équipe de la CRCEN, et suppression des tokens en dehors d'une certaine fréquence) le corpus d'épigrammes. Avec 4218 `instances` en entrée nous obtenons 64637 `tokens` et 36279 `types`. Ce résultat n'a jamais été deux fois le même selon les paramètres utilisés.

![](imagesSCI6203-tp02/preprocessingcorpus.PNG)

- Orange permet d'ores et déjà une première visualisation du corpus sous forme de nuage de mots grâce au widget `Word Cloud`. 

![](imagesSCI6203-tp02/wordCloud.PNG)

- Le widget suivant s'appelle `Bag of Words`, il créé un compteur de la fréquence de chaque terme du corpus.
- `Distances` calcule la distance (cosinus dans notre cas) entre chaque ligne du fichier source : il détermine la proximité entre les lignes.
- `Hierarchical Clustering` offre une visualisation sous forme de cluster des distances calculées précédemment.

![](imagesSCI6203-tp02/hierarchicalClustering.PNG)

- Les deux derniers widgets, `Corpus Viewer` et `MDS` permettent des visualisation plus fines des clusters : en sélection un cluster particulier ou un ensemble de clusters il est possible de les afficher soit sous forme brute dans Corpus Viewer (et voir leur contenus) soit sous forme de graphe avec MDS.

![](imagesSCI6203-tp02/CorpusViewer.PNG)

![](imagesSCI6203-tp02/mds.PNG)


Les résultats que nous obtenons permettent de faire un premier état des lieux sur notre corpus : il nous faut correctement composer ce dernier pour commencer à réellement travailler à la problématique sur les variations. Toutefois, les regroupements par clusters (à partir des distances par cosinus) ne sont pas sans intérêt, en effet, nous remarquons que les clusters regroupent des mot-clefs appartenant à un même champ lexical. Si nous reprenons l'exemple affiché précédemment, les épigrammes du cluster sont articulées autour des mots clefs "Muse", "peinture", "écriture". 
Cette méthode d'apprentissage automatique fait partie de l'ensemble des méthodes non supervisées (conseillée à la fin du TP01) et fera l'objet d'une attention particulière pour les prochains développements de cette étude.
