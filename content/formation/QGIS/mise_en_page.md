---
date: "2019-05-05T00:00:00+01:00"
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

La production de carte est le processus d’arrangement des éléments cartographiques sur une feuille de papier d’une façon que, même sans beaucoup de mots, la personne moyenne puisse comprendre de quoi il s’agit. Les éléments courants d’une carte sont le titre, le corps de carte, la légende, la flèche du nord, l’échelle, les remerciements, et la bordure de la carte.



Avec les mises en page de cartes ou de rapports, vous pouvez créer des cartes et des atlas, les imprimer ou les sauvegarder en tant que fichiers PDF, image ou SVG.


L'outil de mise en page de QGIS ests assez complexe. Au lieu d'explorer les différents menu et fonctionnalités, nous allons créer une carte simple, étape par étape.


## Propriétés de la page

Tout d'abord, on choisi la taille de la page et son orientation. Par défaut la page est de taille A4 (format européen). Il suffit de cliquer droit dans le canvas, de sélectionner `Propriétés de la page`. Un menu apparaît à droite avec les différents options.

![](/img/gif/format_page.gif)

## Ajout d'une carte

Pour ajouter une carte au canvas, il faut cliquer sur l'icone `Ajoute une nouvelle carte à la mise en page`. Un trace ensuite un rectangle oàu l'on souhaite voir la carte.


![](/img/gif/ajout_carte.gif)

## Replacer la position

Si on se déplace sur la carte dans le canevas principal, la carte dans la partie Mise en page n'est pas mise à jour. Toutefois, si on change les styles ou l'ordre des couches, la mise en page est mise à jour (même si ce n'est pas visible à l'écran lorsque vous l'exporter, il aura le style dans le canevas principal). Pour replacer la carte afin qu'elle corresponde avec le canevas principal, cliquer gauche sur la carte, puis dans le menu `Propriétés de l'élément`, cliquer sur le bouton `Régler l'emprise de la carte pour qu'elle corresponde à l'emprise du canevas principal`.

![](/img/gif/replacer_carte.gif)


## Se déplacer sur la carte

Si vous souhaitez déplacer la carte sans passez par le canevas principal, vous pouvez utiliser l'outil `Déplacer le contenu de l'élément`. N'oublier pas de revenir à l'outil de sélection ensuite.


![](/img/gif/deplacer_carte.gif)

## Tourner la carte et changer l'échelle

Sélectionner la carte, à droite dans le menu `Propriétés de l'élément`, vous pouvez définir la rotation et l'échelle de la carte. 


![](/img/gif/tourner_carte.gif)

## Ajouter une échelle

Pour ajouter une échelle, cliquer sur l'outil `Ajouter une échelle graphique à la mise en page`. Ensuite tracer un rectangle ou vous shouhaitez voir l'échelle. En sélectionnant l'échelle, puis en allant dans le menu `Propriétés de l'élément` vous aurez différents options sur le style de l'échelle.

![](/img/gif/echelle.gif)

## Ajouter une rose des vents

Pour ajouter une rose des vents, cliquer sur l'outil `Ajoute une nouvelle Flèche du nord à la mise en page`. Ensuite tracer un rectangle ou vous shouhaitez voir la flèche. En sélectionnant la flèche, puis en allant dans le menu `Propriétés de l'élément` vous aurez différents options sur le style de la flèche.
![](/img/gif/rose.gif)

## Ajouter une légende

Pour ajouter une légende, cliquer sur l'outil `Ajoute une nouvelle Légende à la mise en page`. Ensuite tracer un rectangle ou vous shouhaitez voir la légende. En sélectionnant la légende, puis en allant dans le menu `Propriétés de l'élément` vous aurez différents options sur le style de la légende.

![](/img/gif/legende.gif)


## Ajouter du texte

Pour ajouter une boîte de texte, cliquer sur l'outil `Ajoute une nouvelle Étiquette à la mise en page`. Ensuite tracer un rectangle ou vous shouhaitez voir la boîte de texte. En sélectionnant la boîte de texte, puis en allant dans le menu `Propriétés de l'élément` vous aurez différents options sur le style de la boîte de texte. C'est à cet endroit que vous pourrez inscrire le texte.

![](/img/gif/texte.gif)

## Ajouter un tableau

Pour ajouter un tableau, cliquer sur l'outil `Ajouter une nouvelle Table des attributs à la mise en page`. Ensuite tracer un rectangle ou vous shouhaitez voir le tableau. En sélectionnant le tableau, puis en allant dans le menu `Propriétés de l'élément` vous aurez différents options sur le style du tableau.

* L'onglet couche permet de choisir la table d'attribut de quelle couche est présentée.
* Le bouton `Attributs...` permet de modifier les En-têtes, de supprimer des colonnes de changer l'ordre etc.



![](/img/gif/tableau.gif)

## Exporter en pdf

Dans la barre d'outil du haut cliquer sur `Exporter au format PDF`.

![](/img/gif/pdf.gif)

## Enregistrer un modèle


Faire une belle mise en page est un processus assez long. Je vous conseil d'enregistrer votre mise en page en tant que modèle et de vous les partager entre collègues. 

Pour enregistrer le modèle, cliquer sur l'outil `Enregistrer en tant que modèle` dans la barre d'outil du haut.

![](/img/gif/enregistrer_modele.gif)


## Charger un modèle

Pour charger un modèle, cliquer sur l'outil `Ajouter des éléments depuis un modèle`. Il est probable que vous ayez à replacer la carte, et changer les couches dans la légende et dans le tableau.

![](/img/gif/charger_modele.gif)

## Ajouter une page

Dans votre mise en page, vous ppouvez avoir plusieurs page. Pour en ajouter une, cliquer sur l'outil `Ajouter des pages` dans la barre d'outils du haut. Vous pouvez soit partir de zéro, charger un modèle, ou copier-coller les éléments de votre page précédente. Il est important de noter que les éléments sont souvent associer avec une carte, vous devez aller indiquer sur l'échelle et la rose des vents quelle carte utiliser.



![](/img/gif/ajout_page.gif)
