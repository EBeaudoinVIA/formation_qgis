---
date: "2020-05-19T00:00:00+01:00"
draft: false
linktitle: Mise en page
menu:
  example:
    parent: QGIS
    weight: 8
title: Mise en page
toc: true
type: docs
weight: 8
---

La production de carte est le processus d’arrangement des éléments cartographiques sur une feuille de papier d’une façon dont, même sans beaucoup de mots, la personne moyenne puisse comprendre de quoi il s’agit. Les éléments courants d’une carte sont le titre, le corps de carte, la légende, la flèche du nord, l’échelle, les remerciements, et la bordure de la carte.



Avec les mises en page de cartes ou de rapports, vous pouvez créer des cartes et des atlas, les imprimer ou les sauvegarder en tant que fichiers PDF, image ou SVG.


L'outil de mise en page de QGIS est assez complexe. Au lieu d'explorer les différents menus et fonctionnalités, nous allons créer une carte simple, étape par étape.


## 1- Propriétés de la page

Tout d'abord, on choisit la taille de la page et son orientation. Par défaut la page est de taille A4 (format européen). Il suffit de cliquer droit dans le canevas, de sélectionner `Propriétés de la page`. Un menu apparaît à droite avec les différentes options.

{{< figure library="true" src="gif/format_page.gif" title="Propriétés de la page" lightbox="true" >}}


## 2- Ajouter une carte

Pour ajouter une carte au canevas, il faut cliquer sur l'icône `Ajoute une nouvelle carte à la mise en page`. On trace ensuite un rectangle où l'on souhaite voir la carte.

{{< figure library="true" src="gif/ajout_carte.gif" title="Ajouter une carte" lightbox="true" >}}


## 3- Replacer la position

Si on se déplace sur la carte dans le canevas principal, la carte dans la partie Mise en page n'est pas mise à jour. Toutefois, si on change les styles ou l'ordre des couches, la mise en page est mise à jour (même si ce n'est pas visible à l'écran lorsque vous l'exportez, il aura le style dans le canevas principal). Pour replacer la carte afin qu'elle corresponde avec le canevas principal, cliquer gauche sur la carte, puis dans le menu `Propriétés de l'élément`, cliquer sur le bouton `Régler l'emprise de la carte pour qu'elle corresponde à l'emprise du canevas principal`.

{{< figure library="true" src="gif/replacer_carte.gif" title="Replacer la position" lightbox="true" >}}

## 4- Se déplacer sur la carte

Si vous souhaitez déplacer la carte sans passez par le canevas principal, vous pouvez utiliser l'outil `Déplacer le contenu de l'élément`. N'oubliez pas de revenir à l'outil de sélection ensuite.


{{< figure library="true" src="gif/deplacer_carte.gif" title="Se déplacer sur la carte" lightbox="true" >}}


## 5- Tourner la carte et changer l'échelle

Sélectionner la carte, à droite dans le menu `Propriétés de l'élément`, vous pouvez définir la rotation et l'échelle de la carte. 


{{< figure library="true" src="gif/tourner_carte.gif" title="Tourner la carte et changer l'échelle" lightbox="true" >}}

## 6- Ajouter une échelle

Pour ajouter une échelle, cliquer sur l'outil `Ajouter une échelle graphique à la mise en page`. Ensuite, tracez un rectangle ou vous souhaitez voir l'échelle. En sélectionnant l'échelle, puis en allant dans le menu `Propriétés de l'élément` vous aurez différentes options sur le style de l'échelle.

{{< figure library="true" src="gif/echelle.gif" title="Ajouter une échelle" lightbox="true" >}}

## 7- Ajouter une rose des vents

Pour ajouter une rose des vents, cliquer sur l'outil `Ajoute une nouvelle Flèche du nord à la mise en page`. Ensuite, tracez un rectangle ou vous souhaitez voir la flèche. En sélectionnant la flèche, puis en allant dans le menu `Propriétés de l'élément` vous aurez différentes options sur le style de la flèche.


{{< figure library="true" src="gif/rose.gif" title="Ajouter une rose des vents" lightbox="true" >}}

## 8- Ajouter une légende

Pour ajouter une légende, cliquer sur l'outil `Ajoute une nouvelle Légende à la mise en page`. Ensuite, tracez un rectangle ou vous souhaitez voir la légende. En sélectionnant la légende, puis en allant dans le menu `Propriétés de l'élément` vous aurez différentes options sur le style de la légende.

{{< figure library="true" src="gif/legende.gif" title="Ajouter une légende" lightbox="true" >}}

## 9- Ajouter du texte

Pour ajouter une boîte de texte, cliquer sur l'outil `Ajoute une nouvelle Étiquette à la mise en page`. Ensuite, tracez un rectangle ou vous souhaitez voir la boîte de texte. En sélectionnant la boîte de texte, puis en allant dans le menu `Propriétés de l'élément` vous aurez différentes options sur le style de la boîte de texte. C'est à cet endroit que vous pourrez inscrire le texte.

![](/img/gif/texte.gif)

## 10- Ajouter un tableau

Pour ajouter un tableau, cliquer sur l'outil `Ajouter une nouvelle Table des attributs à la mise en page`. Ensuite, tracez un rectangle ou vous souhaitez voir le tableau. En sélectionnant le tableau, puis en allant dans le menu `Propriétés de l'élément` vous aurez différentes options sur le style du tableau.

* L'onglet couche permet de choisir la table d'attribut de quelle couche est présentée.
* Le bouton `Attributs...` permet de modifier les En-têtes, de supprimer des colonnes de changer l'ordre, etc.



![](/img/gif/tableau.gif)

## 11- Exporter en pdf

Dans la barre d'outil du haut cliquez sur `Exporter au format PDF`.

{{< figure library="true" src="gif/pdf.gif" title="Exporter en pdf" lightbox="true" >}}



## Enregistrer un modèle


Faire une belle mise en page est un processus assez long. Je vous conseille d'enregistrer votre mise en page en tant que modèle et de vous les partager entre collègues. 

Pour enregistrer le modèle, cliquer sur l'outil `Enregistrer en tant que modèle` dans la barre d'outils du haut.



{{< figure library="true" src="gif/enregistrer_modele.gif" title="Enregistrer un modèle" lightbox="true" >}}


## Charger un modèle

Pour charger un modèle, cliquer sur l'outil `Ajouter des éléments depuis un modèle`. Il est probable que vous ayez à replacer la carte, et changer les couches dans la légende et dans le tableau.

{{< figure library="true" src="gif/charger_modele.gif" title="Charger un modèle" lightbox="true" >}}



## Ajouter une page

Dans votre mise en page, vous pouvez avoir plusieurs pages. Pour en ajouter une, cliquer sur l'outil `Ajouter des pages` dans la barre d'outils du haut. Vous pouvez soit partir de zéro, charger un modèle, ou copier-coller les éléments de votre page précédente. Il est important de noter que les éléments sont souvent associés avec une carte, vous devez aller indiquer sur l'échelle et la rose des vents quelle carte utiliser.


{{< figure library="true" src="gif/ajout_page.gif" title="Ajouter une page" lightbox="true" >}}