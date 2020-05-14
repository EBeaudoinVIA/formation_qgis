---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Numérisation
menu:
  example:
    parent: QGIS
    weight: 5
title: Numérisation
toc: true
type: docs
weight: 5
---
## Ajout de couches

* Explorateur
* Menu - Couche
* *Drag and Drop*

## Explorateur

![](/img/gif/ajout_explorateur.gif)


## Menu - Couche

![](/img/gif/ajout_menu.gif)

## *Drag and Drop*

![](/img/gif/ajout_drag.gif)


## Création d'une couche

![](/img/gif/creation.gif)



## Mémoire temporaire

Lors de la création d'une couche, on peut choisir de créer une couche en mémoire temporaire. Si vous choisissez cette option, la couche sera perdu si vous fermez le projet (ou QGIS bogue).

## Numérisation de points, lignes et polygones 

Selon le type de couche, vous pouvez utiliser  capturePoint Ajouter un point, captureLine Ajouter une ligne ou capturePolygon Ajouter un polygone dans la barre d’outils pour ajouter de nouvelles entités dans la couche actuelle.
Pour numériser la géométrie:

Faites un clic gauche sur la zone de la carte pour créer le premier point de votre nouvelle entité. Pour les entités ponctuelles, cela devrait suffire et déclencher, si nécessaire, le formulaire pour renseigner leurs attributs. 

Pour les géométries de ligne ou de polygone, continuez à cliquer avec le bouton gauche de la souris pour chaque point supplémentaire que vous souhaitez capturer ou utiliser

En appuyant sur la touche Del ou Suppr, vous annulez le dernier nœud ajouté.

Lorsque vous avez terminé d’ajouter des points, cliquez avec le bouton droit n’importe où sur la zone de carte pour confirmer que vous avez terminé d’entrer la géométrie de cette entité.


1. Démarrer le mode édition
1. Ajouter une entité
1. Clique droit pour arrêter (ligne et polygone)
1. Saisir l'information
1. Enregistrer
1. Arrêter le mode édition



![](/img/gif/numerisation.gif)

## Exportation 

1. Clique droit
1. Enregistrer sous
1. Choisir le format
1. Choisir le dossier
1. Choisir la projection
1. Enregistrer

## Exportation 


![](/img/gif/exportation.gif)
