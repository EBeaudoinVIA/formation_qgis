---
date: "2019-05-05T00:00:00+01:00"
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
## Couches

La plupart des applications SIG regroupent les entités vectorielles dans des couches. Les entités d’une couche ont le même type de géométrie (par exemple, ils seront tous des points) et les mêmes types d’attributs (par exemple, l’information sur l’espèce d’un arbre au sein d’une couche arbres). Par exemple, si vous avez enregistré les positions de tous les sentiers dans votre école, ils seront généralement stockés ensemble sur le disque dur de l’ordinateur et affichés dans le SIG en une seule couche. C’est pratique, car il vous permet de masquer ou d’afficher toutes les caractéristiques de cette couche dans votre application SIG avec un simple clic de souris.


![](/img/img/misc/couche.png)

::: notes
 United States Geological Survey / Public domain
:::

## Vecteur

Les données vectorielles fournissent un moyen de représenter le monde réel par des entités dans l’environnement SIG. Une entité est une chose que vous pouvez voir dans le paysage. Imaginez que vous êtes debout sur le sommet d’une colline. En regardant en bas, vous pouvez voir des maisons, des routes, des arbres, des rivières, et ainsi de suite (voir figure_vector_landscape). Chacune de ces choses serait une entité quand nous les représentons dans une application SIG. Les données vectorielles ont des attributs, qui se composent d’informations textes ou numériques qui décrivent les entités.

Une entité vectorielle a sa forme représentée en utilisant la géométrie. La géométrie est constituée d’un ou plusieurs sommets interconnectés. Un sommet décrit une position dans l’espace en utilisant un X, Y et éventuellement un axe Z. Les géométries qui ont des sommets avec un axe Z sont souvent désignés comme 2.5D, car ils décrivent la hauteur ou la profondeur de chaque sommet, mais pas les deux.

Lorsque la géométrie d’une entité est composée d’un seul sommet, elle est référencée en tant qu’entité de point (consultez l’illustration figure_geometry_point). Lorsque la géométrie est composée d’un ou plusieurs sommets et que le premier et le dernier ne sont pas égaux, une entité de type polyligne est formée (illustration figure_geometry_polyline). Lorsque trois sommets ou plus sont présents et que le dernier sommet est égal au premier, une entité de polygone fermé est formée (illustration figure_geometry_polygon).




![](/img/img/misc/vecteur_vs_raster.png)

La donnée vectorielle est utilisée pour représenter les entités du monde réel dans un SIG.

Une entité vectorielle peut avoir une géométrie de type point, polyligne ou polygone.

Chaque entité vectorielle a des données attributaires qui la décrivent.

La géométrie de l’entité est décrite en termes de sommets.

Les géométries de type Point sont composées de sommet unique (coordonnées X,Y et éventuellement Z).

Les géométries de type Polyligne sont composées de deux ou plusieurs sommets reliés en ligne.

Les géométries de type Polygone sont construites avec au moins quatre sommets formant une surface close. Les premiers et derniers sommets sont toujours au même endroit.

Le choix du type de géométrie dépend de l’échelle, de sa commodité et de ce que vous voulez faire avec les données dans le SIG.

La plupart des applications SIG ne vous permettent pas de mélanger plus d’un type de géométrie dans une même couche.

La numérisation est le processus de création de données vecteur, en les dessinant au sein d’une application SIG.

Les données vectorielles peuvent présenter des problèmes de qualité comme les croisements, les non-connexions et les écarts dont vous devez connaître l’existence.

Les données vectorielles peuvent être utilisées pour des analyses spatiales dans une application SIG, par exemple pour trouver l’hôpital le plus proche d’une école.
![](/img/img/misc/vecteur.png)

::: notes
 Penn State's College of Earth and Mineral Science
:::

## Entités

* Chaque couche vectorielle peut comporter plusieurs entités.
* Par exemple une couche **Plan de ferme** peut avoir plusieurs polygones de champ.

## Noeuds
* Dans une entité vectorielle, chaque point qui définit l'entité est un noeud. 
* Par exemple pour une ligne droite, j'ai un noeud au début et un noeud à la fin, dans un rectangle j'en aurais 4.
* Chaque noeud est présenté par une paire de coordonnées (Lat 45.24, Lon -72.14)
* Les noeuds peuvent avoir l'espacement qu'un veut

![](/img/img/misc/vecteur.png)

## Champs 

Les attributs d’une entité vectorielle sont stockés dans une table. Une table est comme un tableur. Chaque colonne dans la table est appelée un champ. Chaque ligne dans la table est un enregistrement. La table table_house_attributes montre un exemple simple de ce à quoi ressemble une table attributaire dans un SIG. Les enregistrements dans la table d’attributs dans un SIG correspondent chacun à une entité. Habituellement, l’information de la table attributaire est stockée dans une sorte de base de données. L’application SIG lie les enregistrements des attributs avec l’entité géométrique afin que vous puissiez trouver les enregistrements dans la table en sélectionnant les entités sur la carte, et trouver les entités sur la carte en sélectionnant les entités dans la table.

Chaque champ dans la table attributaire contient un type de données spécifique –– texte, numérique ou date. Décider quels attributs utiliser pour une entité nécessite une certaine réflexion et planification. 

* C’est l’information non spatiale contenue dans la base de données qui est associée à l’entité.
* Dans la formation, on ne va pas utiliser le terme Champs pour désigner cette information pour des raisons évidentes...

![](/img/img/misc/table_attributs.png)

::: notes
 Allison Horst / @allison_horst
:::

## Shapefiles 

Tout comme ces autres applications, les applications SIG peuvent stocker leurs données dans des fichiers sur le disque dur de l’ordinateur. Il y a un certain nombre de formats de fichiers différents pour les données SIG, mais le plus commun est probablement le “shapefile”. Le nom est un peu bizarre, mais bien que nous l’appelons un shapefile (au singulier), il est en fait constitué d’au moins trois fichiers différents qui collaborent ensemble pour stocker vos données numériques vectorielles,


lorsque vous regardez les fichiers qui composent un shapefile sur votre disque dur, vous verrez quelque chose du genre de figure_shapefile. Si vous souhaitez partager de la donnée vectorielle stockée dans un shapefile avec d’autres personnes, il est très important de leur fournir tous les fichiers de cette couche. Cela signifie que, dans l’arborescence présentée dans la figure_shapefile, vous devriez donner à la personne trees.shp, trees.shx, trees.dbf, trees.prj et trees.qml.



* Le shapefile est un format de donnée pour stocker des couches vectorielles. 1 shapefile ne peut contenir qu’une couche.
* Un shapefile est est fait plusieurs fichiers ayant le même nom, mais avec une extension différente:



* .SHP - Stocke l’information spatiale
* .DBF - Stocke l’information non spatiale
* .PRJ - Stocke la projection (pour d’autres logiciels)
* .SHX - Stocke l’index
* .CPG - Stocke l’encodage (type de caractère)
* .qpj - Stock la projection (pour QGIS)


Certains fichiers sont facultatifs, mais pour s’assurer que tout fonctionne le mieux possible, utiliser toujours tous les fichiers.



## Raster
Alors que les entités vectorielles utilisent une géométrie (points, polylignes et polygones) pour représenter le monde réel, les données raster ont une approche différente. Les rasters sont constitués d’une matrice de pixels (également appelés cellules), chacun contenant une valeur qui représente les conditions de la surface couverte par cette cellule (voir figure_raster). Dans ce sujet, nous allons voir de plus près les données raster, quand est-ce nécessaire et quand cela a-t-il plus de sens d’utiliser des données vectorielles.

Les données raster sont utilisées dans une application SIG lorsque nous voulons afficher une information continue sur une surface et qui ne peut pas facilement être divisée en entités vectorielles. Lorsque nous vous avons présenté les données vectorielles, nous vous avons montré l’image dans figure_landscape. Les entités de point, polyligne et polygone fonctionnent bien pour représenter des entités de ce paysage, telles que les arbres, les routes et les empreintes de constructions. D’autres entités dans un paysage peuvent être plus difficilement représentées en utilisant des entités vectorielles. Par exemple, les prairies ont beaucoup de variation de couleur et de densité de couverture. Il serait assez facile de faire un simple polygone autour de chaque surface de prairie, mais beaucoup d’informations sur les prairies seront perdues durant le processus de simplification des entités en un unique polygone. C’est parce que lorsque vous donnez à une entité vectorielle des valeurs d’attribut, elles s’appliquent à toute l’entité, donc les vecteurs ne sont pas très bien pour représenter des entités qui ne sont pas homogènes (entièrement la même) partout. Une autre approche que vous pouvez avoir est de numériser chaque petite variation de couleur d’herbe et de la couvrir par un polygone. Le problème avec cette approche est que cela demande une énorme quantité de travail pour créer un bon jeu de données vectorielles.

Utiliser des données raster est une solution à ces problèmes. Beaucoup de personnes utilisent des données raster comme une toile de fond à utiliser derrière des couches vectorielles afin de fournir plus de sens à l’information vectorielle. L’œil humain est très bon pour interpréter des images, et donc utiliser une image derrière des couches vectorielles donne des résultats dans les cartes avec beaucoup plus de sens. Les données raster ne sont pas seulement bonnes pour les images qui dépeignent la surface du monde réel (par ex. les images satellites et les photographies aériennes), elles sont aussi bonnes pour représenter des idées plus abstraites. Par exemple, des rasters peuvent être utilisés pour montrer les tendances des précipitations dans une zone, ou pour représenter le risque d’incendie dans un paysage. Dans ces types d’applications, chaque cellule du raster représente une valeur différente, par ex. un risque d’incendie sur une échelle d’un à dix.


Les données rasters sont une grille de pixels à taille régulière.

Les données raster sont bien pour montrer de l’information continuellement variable.

La taille des pixels dans un raster détermine sa résolution spatiale.

Des images raster peuvent contenir une ou plusieurs bandes, chacune couvrant la même aire spatiale, mais contenant des informations différentes.

Lorsque des données raster contiennent des bandes de différentes parties du spectre électromagnétique, elles sont appelées images multispectrales.

Trois des bandes d’une image multispectrale peuvent être montrées dans les couleurs Rouge, Verte et Bleue de sorte que nous puissions les voir.

Des images avec une bande unique sont appelées images en niveaux de gris.

À bande unique, les images en niveaux de gris peuvent être montrées en pseudo-couleur par les SIG.

Les images Raster peuvent consommer beaucoup d’espace de stockage.


![](/img/img/misc/raster.png)

## Vecteurs vs Raster

* Le type d’analyse qu’on peut faire va changer si l’information est sous forme de point, de ligne, de polygone ou de raster

* On ne peut mesure la superficie d’un point alors qu’on peut avec un polygone
* On ne peut additionner des polygones alors qu’on peut avec des raster

* Dans cette formation, nous n’approfondirons pas les analyses avec des Raster. Ceux-ci sont moins utiles pour l’usage de base en géomatique.

