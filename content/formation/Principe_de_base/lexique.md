---
date: "2020-05-19T00:00:00+01:00"
draft: false
linktitle: Lexique
menu:
  example:
    parent: Principes de base
    weight: 2
title: Lexique
toc: true
type: docs
weight: 2
---

Voici une liste de termes utilisés en géomatique.


## Couches ou calques

La plupart des applications SIG (système d’information géographique) regroupent les entités vectorielles dans des couches. Les entités d’une couche ont le même type de géométrie (par exemple, ils seront tous des points) et les mêmes types d’attributs (par exemple, l’information sur l’espèce d’un arbre au sein d’une couche arbres).

{{< figure library="true" src="/img/misc/couche.png" title="Source: United States Geological Survey / Public domain" lightbox="false" >}}






## Vecteur vs raster

Lorsque vous utilisez un SIG (pensez à Google Map), l'information peut être présentée sous forme de raster ou sous forme de vecteur. Prenons une route. Dans Google Map, la route peut être représentée par une ligne droite, de couleur et de taille uniformes. C'est un vecteur. En même temps, on peut regarder une image aérienne de cette même route. Soudain, elle paraît beaucoup moins uniforme. On voit des accotements, des trous dans la chaussée, etc. C'est un raster. Ce que nous pouvons faire avec une couche va largement dépendre du fait que l'information soit stockée sous forme de raster ou de vecteur. Pensez à un chemin de ferme. Vous le voyez clairement sur Google Map, mais puisqu'il n'a pas été transformé en vecteur, il ne vous calculera pas d'itinéraire en passant par ce chemin. Si vous regardez un champ en raster, vous allez voir la variabilité de la couleur et de la densité. En vecteur, ce même champ ne serait représenté que par 1 polygone, donc par une seule valeur.


Sur cette carte, vous voyez une moitié en raster et une moitié en vecteur. Remarquez que, même si c'est au même endroit, l'information qu'on peut en extraire est complètement différente.

<iframe src="/img/figure.html" style="width: 100%; height: 500px; border:0;"></iframe>

## Vecteur


{{< figure library="true" src="/img/misc/vecteur_vs_raster.png" title="Même type d'information stockée soit en vecteur ou en raster. Source: Penn State's College of Earth and Mineral Science" lightbox="false" >}}



* La donnée vectorielle est utilisée pour représenter les entités du monde réel dans un SIG.

* Une entité vectorielle peut avoir une géométrie de type point, polyligne ou polygone.

* Chaque entité vectorielle a des données attributaires qui la décrivent.

* La géométrie de l’entité est décrite en termes de sommets.

* Les géométries de type point sont composées de sommets uniques (coordonnées X,Y et éventuellement Z).

* Les géométries de type polyligne sont composées de deux ou plusieurs sommets reliés par une ligne.

* Les géométries de type polygone sont construites avec au moins quatre sommets formant une surface close. Les premiers et derniers sommets sont toujours au même endroit.

* Le choix du type de géométrie dépend de l’échelle, de sa commodité et de ce que vous voulez faire avec les données dans le SIG.


 



## Entités

Les données vectorielles fournissent un moyen de représenter le monde réel par des entités dans l’environnement SIG. Une entité est une chose que vous pouvez voir dans le paysage. Imaginez que vous êtes debout sur le sommet d’une colline. En regardant en bas, vous pouvez voir des maisons, des routes, des arbres, des rivières, et ainsi de suite. Chacune de ces choses serait une entité quand nous la représentons dans une application SIG. Les données vectorielles ont des attributs, qui se composent d’informations textes ou numériques qui décrivent les entités.



* Chaque couche vectorielle peut comporter plusieurs entités.
* Par exemple une couche **Plan de ferme** peut avoir plusieurs polygones de parcelles.

## Noeuds, sommets, arêtes, segments

Les entités sont constituées d’un ou plusieurs sommets (ou noeuds) interconnectés. Un sommet décrit une position dans l’espace en utilisant un X, Y et éventuellement un axe Z. Pour une ligne droite, on a deux sommets reliés par une ligne appelée arête ou segment. Une ligne peut être formée de plusieurs segments.


{{< figure library="true" src="/img/misc/vecteur.png" title="Remarquez les points rouges : ce sont les nœuds. Entre les points, le segment est droit. Ainsi, si on veut représenter une entité plus arrondie, on doit augmenter le nombre de segments. Source: Penn State's College of Earth and Mineral Science" lightbox="false" >}}


## Champs, colonnes, attributs

Les attributs d’une entité vectorielle sont stockés dans une table. Une table est comme un tableur (pensez à une feuille Excel). Chaque colonne dans la table est appelée un champ ou un attribut. Chaque ligne dans la table correspond à une entité.


Chaque champ dans la table attributaire contient un type spécifique de données (texte, numérique ou date). Décider quels attributs utiliser pour une entité nécessite une certaine réflexion et planification. 


{{% alert note %}}

Dans la formation, on ne va pas utiliser le terme Champs pour désigner cette information pour des raisons évidentes...
{{% /alert %}}
 

{{< figure library="true" src="/img/misc/table_attributs.png" title="La meilleure façon de comprendre la table attributaire est d'imaginer un tableau Excel auquel on aurait collé une forme. Source: Allison Horst / @allison_horst" lightbox="false" >}}

## Shapefiles 

Il y a un certain nombre de formats de fichiers différents pour les données SIG, mais le plus commun est probablement le « shapefile ». Le nom est un peu bizarre, mais bien que nous l’appelions un shapefile (au singulier), il est en fait constitué d’au moins trois fichiers différents qui collaborent pour stocker vos données numériques vectorielles.

Si vous souhaitez partager de la donnée vectorielle stockée dans un shapefile avec d’autres personnes, il est très important de leur fournir tous les fichiers de cette couche. 


* .SHP - Stocke l’information spatiale
* .DBF - Stocke l’information non spatiale
* .PRJ - Stocke la projection (pour d’autres logiciels)
* .SHX - Stocke l’index
* .CPG - Stocke l’encodage (type de caractère)
* .qpj - Stocke la projection (pour QGIS)


Certains fichiers sont facultatifs, mais pour s’assurer que tout fonctionne le mieux possible, utilisez toujours tous les fichiers.

Il existe d'autres formats de données vectorielles (.kml, .kmz, .gpkg, .sqlite, .fgdb, .gpx, .dxf), mais le shapefile est certainement le plus courant.


## Raster

Alors que les entités vectorielles utilisent une géométrie (points, polylignes et polygones) pour représenter le monde réel, les données raster ont une approche différente. Les rasters sont constitués d’une matrice de pixels (également appelés cellules), chacun contenant une valeur qui représente les conditions de la surface couverte par cette cellule.


Les données raster sont utilisées dans une application SIG lorsque nous voulons afficher une information continue sur une surface et qui ne peut pas facilement être divisée en entités vectorielles. 

Les entités de points, polylignes et polygones fonctionnent bien pour représenter des entités de paysage, telles que les arbres, les routes et les empreintes de constructions. D’autres entités dans un paysage peuvent être plus difficilement représentées en utilisant des entités vectorielles. 

Par exemple, les prairies ont beaucoup de variation de couleurs et de densités de couverture. Il serait assez facile de faire un simple polygone autour de chaque surface de prairie, mais beaucoup d’informations sur les prairies seront perdues durant le processus de simplification des entités en un unique polygone. En effet, lorsque vous donnez à une entité vectorielle des valeurs d’attributs, elles s’appliquent à toute l’entité. Ainsi, les vecteurs ne sont pas très bons pour représenter des entités qui ne sont pas homogènes (entièrement la même). 

Une autre approche que vous pouvez avoir est de numériser chaque petite variation de couleur d’herbe et de la couvrir par un polygone. Le problème avec cette approche est que cela demande une énorme quantité de travail pour créer un bon jeu de données vectorielles.



Beaucoup de personnes utilisent des données raster comme une toile de fond derrière des couches vectorielles afin de fournir plus de sens à l’information vectorielle.



* Les données rasters sont une grille de pixels de taille régulière.

* Les données raster sont bonnes pour montrer de l’information variable.

* La taille des pixels dans un raster détermine sa résolution spatiale.

* Des images raster peuvent contenir une ou plusieurs bandes, chacune couvrant la même aire spatiale, mais contenant des informations différentes.

* Lorsque des données raster contiennent des bandes de différentes parties du spectre électromagnétique, elles sont appelées images multispectrales.

* Les images raster peuvent consommer beaucoup d’espace de stockage.

{{< figure library="true" src="/img/misc/raster.png" title="Les rasters sont comparables à une photographie numérique : plus on grossit l'image, plus on voit des *pixels* carrés apparaître. Source: Penn State's College of Earth and Mineral Science" lightbox="true" >}}


## Vecteurs vs rasters


* Le type d’analyses qu’on peut faire va changer si l’information est sous forme de points, de lignes, de polygones ou de rasters.
 
* On ne peut pas mesurer la superficie d’un point, alors qu’on peut avec un polygone.

* On ne peut pas additionner des polygones, alors qu’on peut avec des rasters.

*Dans cette formation, nous n’approfondirons pas les analyses avec des rasters.*



