---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Style
menu:
  example:
    parent: QGIS
    weight: 7
title: Style
toc: true
type: docs
weight: 7
---

Lorsqu’une couche est ajoutée au canevas de carte, QGIS utilise un symbole/couleur aléatoire pour le rendu de ses entités. Vous pouvez néanmoins paramétrer un symbole par défaut dans menuselection:Projet –> Propriétés –> Styles par défaut qui sera appliqué à chaque nouvel ajout de couche selon le type géométrique de cette dernière.

Cependant, la plupart du temps, vous voudrez disposer d’un style plus complexe et plus personnalisé qui pourra être appliqué automatiquement ou manuellement (mais avec moins d’effort). Vous pouvez y parvenir en utilisant la liste déroulante Style située en bas de la boîte de dialogue des Propriétés de la couche. Cette liste déroulante vous permet de créer, de charger et de gérer les styles.

Un style enregistre toute information renseignée dans la boîte de dialogue des propriétés de la couche pour effectuer le rendu ou l’interaction avec la couche (comprenant les paramètres de la symbologie, de l’étiquetage, des formulaires, des actions, des diagrammes,etc.) pour les couches vectorielles, ou les pixels (bande et rendu de couleurs, opacité, pyramides, histogrammes…) pour les rasters.


## Symbologie
Si une entité est symbolisée sans utiliser les données de la table attributaire, elle peut seulement être symbolisée d’une façon simple. Par exemple avec des entités de point, vous pouvez configurer la couleur et le symbole (cercle, carré, étoile, etc.) mais c’est tout. 
The Symbol selector is the main dialog to design a symbol. You can create or edit Marker, Line or Fill Symbols.

A symbol can consist of several Symbol layers. The symbol tree shows the overlay of these symbol layers that are combined afterwards to shape a new global symbol. Besides, a dynamic symbol representation is updated as soon as symbol properties change.

Depending on the level selected in the symbol tree items, various tools are made available to help you manage the tree:



## Symbologie

![](/img/gif/symbologie.gif)

## Symbologie par catégorie
Parfois, les entités vectorielles représentent des choses avec une valeur numérique changeante. Les lignes de contours sont un bon exemple de cela. Chaque contour possède en général une valeur attributaire appelée “hauteur”, qui contient de l’information sur quelle hauteur ce contour représente. Précédemment dans ce sujet, nous avons montré des contours tous dessinés avec la même couleur. Ajouter une couleur aux contours peut nous aider à interpréter le sens des contours. Par exemple, nous pouvons dessiner des zones de basse altitude avec une couleur, des zones de moyenne altitude avec une autre couleur et des zones de haute altitude avec une troisième couleur.
On peut également faire varier la symbologie par catégorie ou gradué.

## Symbologie par catégorie

![](/img/gif/symbologie_categorie.gif)




## Etiquettes

The Style Manager dialog allows you to create a set of labels or text formats (ie the appearance of the text, including font, size, colors, shadow, background…). Each of these items could later be applied to layers in the labeling Labels tab of the vector Layer Properties dialog or Layer Styling panel or using the labeling Layer Labeling Options button of the Labels toolbar. You can also directly configure them in the abovementioned dialogs.

The Label Settings dialog allows you to configure smart labeling for vector layers. Setting a label includes configuring the text format, and how the label relates with the features or other labels (through placement, rendering and callout).
![](/img/gif/etiquette.gif)


## Enregistrer un style

## Charger un style
