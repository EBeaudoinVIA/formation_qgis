---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Table d'attributs
menu:
  example:
    parent: QGIS
    weight: 4
title: Table d'attributs
toc: true
type: docs
weight: 4
---


La table d’attributs affiche des informations sur les entités d’un calque sélectionné. Chaque ligne du tableau représente une entité (avec ou sans géométrie) et chaque colonne contient une information particulière sur cette entité. Les entités du tableau peuvent être recherchées, sélectionnées, déplacées ou même modifiées.





## Ouvrir la table d'attribut

Pour ouvrir la table attributaire d’une couche vectorielle, activez la couche en cliquant dessus depuis le panneau Couches. Puis dans le menu Couche, cliquez sur ![](/img/img/bouton/mActionOpenTable.png) Ouvrir la table d’attributs. Vous pouvez aussi y accéder avec un clic droit sur la couche puis en sélectionnant ![](/img/img/bouton/mActionOpenTable.png) Ouvrir la table d’attributs ou en cliquant sur le bouton ![](/img/img/bouton/mActionOpenTable.png) Ouvrir la table d’attributs dans la barre d’outils des Attributs. 


![](/img/gif/ouvrir_table_attributs.gif)

L’édition des valeurs attributaires peut être faite en :

* saisissant directement la nouvelle valeur dans la cellule, que la table attributaire soit en mode table ou en mode formulaire. Les modifications sont ainsi faites cellule par cellule, entité par entité ;

* utilisant la calculatrice de champs : pour mettre à jour dans une ligne un champ déjà existant ou un champ à créer, mais pour plusieurs entités.

* utilisant barre de calcul rapide de champ : comme ci-dessus, mais uniquement pour un champ existant.

1. Démarrer le mode édition
1. Saisire l'information
1. Cliquer ailleurs ou `Enter`
1. Enregistrer
1. Arrêter le mode édition


![](/img/gif/editer_table_attributs.gif)




## Ajout et suppression de colonne

1. Démarrer le mode édition
1. Ajouter une colonne
1. Choisir le type d'information
1. Enregistrer
1. Arrêter le mode édition


![](/img/gif/ajouter_colonne.gif)

## Aire et longueur


Sélectionner le champ à mettre à jour dans le menu déroulant.

Remplir la fenêtre de texte avec une valeur, que ce soit une expression saisie à la main ou en la construisant grâce au bouton ![](/img/img/bouton/mActionCalculateField.png) expression.

Cliquer sur le bouton Tout mettre à jour, Mettre à jour la sélection ou Mise à jour filtrée selon vos besoins.

Pour calculer la superficie, utiliser l'expression `$area`. Par défaut, la superficie est calculée en m². Il est possible de changer l'unité par défaut, mais on peut tout aussi bien effectuer la transformation à même l'expression: `$area / 10000`. On peut également le nombre de décimal en utilisant `format_number($area / 10000, 2)` pour obtenir 2 décimales. 


Il est également possible d'ajouter la superficie à partir de la boîte à outils en utilisant la fonction `Ajouter les attributs de géométrie`


Pour les longueurs, c'est le même principe seulement `$length` à la place.

Il est important de recalculer les superficies ou les longueurs lorsqu'on modifie les géométries.

![](/img/gif/calc_aire.gif)
