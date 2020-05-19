---
date: "2020-05-19T00:00:00+01:00"
draft: false
linktitle: Interface
menu:
  example:
    parent: QGIS
    weight: 1
title: Interface
toc: true
type: docs
weight: 1
---

## Barre de menu
![](/img/img/interface/barre_menu.png)

La barre de menu permet d’accéder aux fonctions de QGIS à l’aide de menus hiérarchiques standards. 
La plupart des options de menu ont un outil correspondant et vice-versa. Cependant, les menus ne sont pas organisés exactement comme les barres d’outils. L’emplacement des options de menu dans les barres d’outils est indiqué dans le tableau ci-dessous. Les extensions peuvent ajouter de nouvelles options aux menus. 

### Projet

Le menu Projet fournit les points d’accès et de sortie du fichier projet. Il fournit les outils pour :

* Créer un nouveau fichier de projet à partir de zéro ou en utilisant un autre fichier projet comme modèle.

* Ouvrir un projet à partir d’un fichier, un GeoPackage ou une base de données PostgreSQL

* Fermer un projet ou le ramener à son dernier état sauvegardé

* Enregistrer un projet au format .qgs ou .qgz, dans un fichier ou dans un GeoPackage ou une base de données PostgreSQL

* Exporter le canevas de carte dans différents formats ou utiliser les mises en page pour des sorties plus complexes.

* Régler les propriétés du projet et les options d’accrochage pour l’édition de la géométrie.

### Éditer

Le menu Éditer fournit la plupart des outils natifs nécessaires pour éditer les attributs ou la géométrie des couches.

### Vue


Créez de nouvelles vues cartographiques 2D ou 3D à côté du canevas de carte principal.

* Zoomer ou se déplacer n’importe où

* Interroger les attributs ou la géométrie des entités affichés

* Améliorez l’affichage de la carte avec des modes de prévisualisation, des annotations ou des décorations.

Accédez à n’importe quel panneau ou barre d’outils

Le menu vous permet également de réorganiser l’interface QGIS elle-même à l’aide d’actions telles que :

* Basculer en mode plein écran: couvre tout l’écran tout en masquant la barre de titre

* Basculer la visibilité des panneaux: affiche ou masque les panneaux activés - utile lors de la numérisation d’entités (pour une visibilité maximale du canevas) ainsi que pour les présentations (projetées/enregistrées) utilisant le canevas principal de QGIS

* Basculer en affichage carte plein écran : cache les panneaux, les barres d’outils, les menus et la barre d’état et affiche uniquement le canevas de la carte. Combiné avec l’option plein écran, il permet à votre écran d’afficher uniquement la carte.


### Couche

Le menu Couche fournit un grand nombre d’outils pour créer de nouvelles sources de données, les ajouter au projet ou enregistrer leurs modifications. 

### Préférences

Le menu Préférences permet d'accéder à différents menus d'options.

### Extensions

Le menu extension permet de télécharger, de désactiver, de mettre à jour des extensions. De plus, certaines extensions seront ajoutées à ce menu une fois installé


### Vecteur

Par défaut, QGIS ajoute des algorithmes de Processing au menu Vecteur, groupés par sous-menus. Cela fournit des raccourcis pour de nombreuses tâches SIG vectorielles courantes de différents fournisseurs de traitements.

### Raster

Par défaut, QGIS ajoute des algorithmes de Processing au menu Raster, groupés par sous-menus. Il s’agit d’un raccourci pour de nombreuses tâches SIG raster courantes de différents fournisseurs de traitements.

## Barres d’outils

![](/img/img/interface/barre_outils.png)

Les barres d’outils permettent d’accéder à la plupart des fonctions des menus, ainsi qu’à des outils supplémentaires pour interagir avec la carte. Chaque barre d’outils dispose d’une aide contextuelle. Passez votre souris sur l’élément et une courte description de l’objectif de l’outil s’affichera.

Chaque barre d’outils peut être déplacée selon vos besoins. Vous pouvez les désactiver à partir du menu contextuel qui s’affiche d’un clic droit de la souris sur la barre d’outils.

## Explorateur
![](/img/img/interface/explorateur.png)

L'explorateur  est l’un des principaux moyens d’ajouter rapidement et facilement vos données à des projets.

## Couches
![](/img/img/interface/gestionnaire_couches.png)

Par défaut, les couches montrées dans le canevas de la carte sont dessinés suivant l’ordre dans le panneau de Couches : plus haut est la couche dans le panneau, plus il sera élevé (donc plus visible) dans la vue de la carte

## Barre d’état
![](/img/img/interface/barre_etat.png)

La barre d’état vous fournit des informations générales sur le visualiseur de carte et les actions traitées ou disponibles, et vous offre des outils pour gérer le visualiseur de carte.

Sur le côté gauche de la barre d’état, la barre de localisation, un widget de recherche rapide, vous aide à trouver et à exécuter toutes les fonctions ou options du QGIS. Tapez simplement le texte associé à l’élément que vous recherchez (nom, tag, mot-clé…) et vous obtenez une liste qui se met à jour au fur et à mesure que vous écrivez. Vous pouvez également limiter la portée de la recherche en utilisant les filtres de localisation. Cliquez sur le bouton search pour sélectionner l’un d’entre eux et appuyez sur Configurer pour avoir les paramètres globaux.

Dans la zone située à côté de la barre de localisation, un résumé des actions que vous avez effectuées s’affichera si nécessaire (comme la sélection d’entités dans un calque, la suppression d’un calque) ou une description longue de l’outil sur lequel vous passez la souris (non disponible pour l’ensemble des outils).

En cas d’opérations de longue durée, telles que la collecte de statistiques de couches raster, l’exécution d’algorithmes de traitement ou le rendu de plusieurs couches dans la vue de carte, une barre de progression est affichée dans la barre d’état.


À côté de l’affichage des coordonnées se trouve l’affichage Échelle. Il montre l’échelle de la carte. Il y a un sélecteur qui vous permet de choisir des échelles prédéfinies et personnalisées.


À droite de la loupe, vous pouvez définir un angle de rotation horaire en degrés à appliquer à la carte.

Sur le côté droit de la barre d’état, il y a une petite case à cocher qui peut être utilisée temporairement pour empêcher le rendu des couches dans le Visualisateur de carte .

À droite des fonctions de rendues, vous trouvez le bouton projectionEnabled code EPSG montrant le SCR du projet courant. Cliquer sur ce bouton ouvre la boîte de dialogue Propriétés du projet et vous permet d’appliquer un autre SCR.



## Boîte à outils
![](/img/img/interface/boite_outils.png)


La Boîte à outils de traitement est l’élément principal de l’interface graphique de traitement, et celui que vous êtes le plus susceptible d’utiliser dans votre travail quotidien. Il affiche la liste de tous les algorithmes disponibles regroupés dans différents blocs appelés Fournisseurs, et modèles et scripts personnalisés que vous pouvez ajouter pour étendre l’ensemble des outils. La boîte à outils est donc le point d’accès pour les exécuter, que ce soit en tant que processus unique ou en tant que processus par lots impliquant plusieurs exécutions du même algorithme sur différents ensembles d’entrées.

::: notes
Il est possible que vous ne voyiez pas cette barre. Nous aborderons le sujet plus tard.
:::

## Sélection du projet
![](/img/img/interface/menu_projet.png)
 
La fenêtre de sélection de projets apparaît lorsqu'on démarre QGIS sans démarrer de projet. Il indique les derniers projets ouverts. C'est une façon rapide de rouvrir un projet récent. Une fois un projet choisit ou suite à l'ajout d'une couche, cette fenêtre laisse place au canevas de la carte.


::: notes
Parfois une autre boîte est présente indiquant les nouvelles versions ou les évènements à venir
:::

## Ajouter la barre d'outils de numérisation avancée

La barre d'outils de numérisation avancée contient des outils très utiles, nous allons les utiliser durant la formation. Je vous conseille de l'ajouter (si vous ne le faites pas, vous allez avoir de la misère à suivre). 

Pour l'ajouter, cliquer droit sur la barre d'outils et dans la section **Barre d'outils** et non dans la section **Panneaux**, activer la numérisation avancée.


![](/img/img/misc/numerisation_avancee.png)



## Boutons

| Icone                                      |   Utilisation   |
| -------------                              |:-------------:|
| ![](/img/img/bouton/mActionPan.png)        | Se déplacer dans la carte |
| ![](/img/img/bouton/mActionIdentify.png)   | Identifier les entités      |
| ![](/img/img/bouton/mActionMeasure.png)   | Mesurer une longueur      |
| ![](/img/img/bouton/mActionMeasureArea.png)   | Mesurer une superficie      |
| ![](/img/img/bouton/mActionZoomFullExtent.png)   | Zoomer sur l'ensemble des couches      |
| ![](/img/img/bouton/mActionZoomToLayer.png)   | Zoomer sur la couche sélectionnée      |
| ![](/img/img/bouton/mActionZoomToSelected.png)   | Zoomer sur la sélection      |
| ![](/img/img/bouton/mActionSelectRectangle.png)   | Sélectionner à l'aide d'un rectangle      |
| ![](/img/img/bouton/mActionSelectPolygon.png)   | Sélectionner selon un polygone      |
| ![](/img/img/bouton/mActionToggleEditing.png)   | Démarrer l'édition de la couche      |
| ![](/img/img/bouton/mActionCapturePoint.png)   | Ajouter un point      |
| ![](/img/img/bouton/mActionCaptureLine.png)   | Ajouter une ligne      |
| ![](/img/img/bouton/mActionCapturePolygon.png)   | Ajouter un polygone      |
| ![](/img/img/bouton/mActionMoveFeaturePoint.png)   | Déplacer un point      |
| ![](/img/img/bouton/mActionMoveFeatureLine.png)   | Déplacer une ligne      |
| ![](/img/img/bouton/mActionMoveFeature.png)   | Déplacer un polygone      |
| ![](/img/img/bouton/mActionSplitFeatures.png)   | Diviser une entité      |
| ![](/img/img/bouton/mActionMergeFeatures.png)   | Fusionner des entités      |
| ![](/img/img/bouton/mActionVertexToolActiveLayer.png)   | Éditer les noeuds      |
| ![](/img/img/bouton/mActionLayoutManager.png)   | Ouvrir la mise en page      |
