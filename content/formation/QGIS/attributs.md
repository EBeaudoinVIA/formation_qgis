---
date: "2020-05-19T00:00:00+01:00"
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


La table d’attributs affiche des informations sur les entités d’une couche sélectionnée. Chaque ligne du tableau représente une entité (avec ou sans géométrie) et chaque colonne contient une information particulière sur cette entité. Les entités du tableau peuvent être recherchées, sélectionnées, déplacées ou même modifiées.





## Ouvrir la table d'attribut

Pour ouvrir la table attributaire d’une couche vectorielle, activez la couche en cliquant dessus depuis le panneau Couches.  Vous pouvez aussi y accéder avec un clic droit sur la couche puis en sélectionnant ![](/img/img/bouton/mActionOpenTable.png).


{{< figure library="true" src="gif/ouvrir_table_attributs.gif" title="Ouvrir la table d'attribut" lightbox="true" >}}

L’édition des valeurs attributaires peut être faite en :

* saisissant directement la nouvelle valeur dans la cellule. Les modifications sont ainsi faites cellule par cellule, entité par entité ;

* utilisant la calculatrice de champs

* utilisant barre de calcul rapide de champ


## Saisir de l'information

1. Démarrez le mode édition
1. Saisissez l'information
1. Cliquez ailleurs ou `Enter`
1. Enregistrez
1. Arrêtez le mode édition


{{< figure library="true" src="gif/editer_table_attributs.gif" title="Éditer la table d'attribut" lightbox="true" >}}



## Ajout et suppression de colonne



1. Démarrez le mode édition
1. Ajoutez une colonne
1. Choisissez le type d'information
1. Enregistrez
1. Arrêtez le mode édition


{{< figure library="true" src="gif/ajouter_colonne.gif" title="Ajout et suppression de colonne" lightbox="true" >}}

## Aire et longueur


1. Sélectionnez le champ à mettre à jour dans la barre de calcul rapide de champ.
1.Cliquez sur le bouton `Tout mettre à jour`, `Mettre à jour la sélection` ou `Mise à jour filtrée` selon vos besoins.
1.Pour calculer la superficie, utilisez l'expression `$area`. 


Par défaut, la superficie est calculée en m². Il est possible de changer l'unité par défaut, mais on peut tout aussi bien effectuer la transformation à même l'expression: `$area / 10000`. On peut également choisir le nombre de décimal en utilisant `format_number($area / 10000, 2)`.


Il est également possible d'ajouter la superficie à partir de la boîte à outils en utilisant la fonction `Ajouter les attributs de géométrie`


Pour les longueurs, c'est le même principe seulement `$length` à la place.

{{% alert warning %}}

Il est important de recalculer les superficies ou les longueurs lorsqu'on modifie les géométries.

{{% /alert %}}


{{< figure library="true" src="gif/calc_aire.gif" title="Aire et longueur" lightbox="true" >}}