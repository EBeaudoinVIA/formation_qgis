---
date: "2020-05-19T00:00:00+01:00"
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

 Une des premières tâches que vous allez faire sur QGIS est d'ajouter une couche. Il existe plusieurs méthodes pour en ajouter, aucune n'est vraiment meilleure qu'une autre, c'est selon votre préférence.
 
 
### *Drag and Drop*


Une des façons les plus simples d'ajouter une couche dans le projet est de sélectionner la couche (.shp ou .dbf) dans l'explorateur de fichiers, et en maintenant le clic gauche enfoncé, la glisser dans la fenêtre de QGIS. Il est possible de le faire avec un dossier aussi, une fenêtre vous demandera quelle couche vous souhaitez ajouter parmi toutes les couches disponibles dans le dossier.

{{< figure library="true" src="gif/ajout_drag.gif" title="Drag and Drop" lightbox="true" >}}

### Explorateur

Si vous ne souhaitez pas quitter la fenêtre de QGIS, vous pouvez naviguer vers votre couche en utilisant le panneau explorateur. Vous devez naviguer vers la couche que vous voulez puis double cliquer dessus pour l'ajouter.



{{< figure library="true" src="gif/ajout_explorateur.gif" title="Explorateur" lightbox="true" >}}

### Menu - Couche

Finalement, on peut ajouter des couches en utilisant le menu Couche dans la barre de menus. Ou en cliquant sur l'icône correspondante. Personnellement je n'utilise cette méthode que pour ajouter des connexions WMS/WFS (nous le verrons plus tard).


{{< figure library="true" src="gif/ajout_menu.gif" title="Menu - Couche" lightbox="true" >}}


## Création d'une couche

Pour créer une nouvelle couche vectorielle, la façon la plus simple est d'utiliser le menu Couche ou l'icône correspondante. Un menu apparaîtra vous demandant où enregistrer la couche ainsi que les attributs que vous désirez.


{{< figure library="true" src="gif/creation.gif" title="Création d'une couche" lightbox="true" >}}


## Mémoire temporaire

Lors de la création d'une couche, on peut choisir de créer une couche en mémoire temporaire. Si vous choisissez cette option, la couche sera perdue lors de la fermeture du projet (ou si QGIS bogue). Ça peut tout de même utile pour éviter de créer une immense quantité de fichiers qui ne servent à rien.

Par exemple, si je veux obtenir des points le long d'une ligne, je vais créer ma ligne en mémoire temporaire, créer mes points le long de cette ligne et enregistrer mon fichier de points. La ligne sera perdue, mais elle ne m'était plus utile pour ce que je voulais faire.

Assurez-vous que si vous utilisez cette méthode que la couche qui sera perdue ne servira absolument plus.




## Numérisation de points, lignes et polygones 


Par défaut, QGIS charge les couches en lecture seule : c’est une sécurité pour éviter d’éditer accidentellement une couche. 

Toutes les sessions d’édition commencent en cliquant sur le crayon que l’on trouve dans le menu contextuel de la couche en question, dans la boîte de dialogue de la table d’attributs, **dans la barre d’outils de numérisation** ou encore dans le menu Éditer.


Pour numériser la géométrie:

1. Sélectionnez la couche ou vous souhaitez ajouter une entité.

1. Démarrez le mode édition en cliquant sur le crayon.

1. Sélectionnez l'outil d'ajout d'entité (la forme de l'icône dépend du type de géométrie)

1. Faites un clic gauche sur la zone de la carte pour créer le premier point de votre nouvelle entité. Pour les entités ponctuelles, cela devrait suffire et déclencher, si nécessaire, le formulaire pour renseigner leurs attributs. 

1. Pour les géométries de ligne ou de polygone, continuez à cliquer avec le bouton gauche de la souris pour chaque point supplémentaire que vous souhaitez capturer ou utiliser

1. En appuyant sur la touche Del ou Suppr, vous annulez le dernier nœud ajouté.

1. Lorsque vous avez terminé d’ajouter des points, cliquez avec le clic droit n’importe où sur la zone de carte pour confirmer que vous avez terminé d’entrer la géométrie de cette entité.

1. Saisissez l'information

1. Enregistrez les modifications en cliquant sur la disquette à côté du crayon.
1. Arrêtez le mode édition en cliquant sur le crayon.



{{< figure library="true" src="gif/numerisation.gif" title="Numérisation de points, lignes et polygones" lightbox="true" >}}

## Exportation 

Si vous souhaitez exporter votre couche vers un nouveau fichier, par exemple si vous aviez une couche en mémoire temporaire et que finalement vous souhaitez l'enregistrer, vous devez:


1. Cliquez droit sur la couche à exporter
1. Sélectionnez `Enregistrer sous` 
1. Choisissez le format `ESRI Shapefiles`
1. Choisissez le dossier et nommez le fichier
1. Choisissez la projection
1. Si vous souhaitez seulement exporter la sélection, vous pouvez cocher la case `N'enregistrer que les entités sélectionnées`
1. Cliquez sur `OK`



{{< figure library="true" src="gif/exportation.gif" title="Exportation" lightbox="true" >}}

## Changer la projection d'une couche

Si vous souhaitez modifier la projection d'une couche, la façon la plus simple est d'exporter la couche. Au moment d'enregistrer, choisir la projection désirée. Vous pouvez ensuite supprimer les fichiers originaux pour éviter de vous mêler. Si vous voulez supprimer des fichiers, vous devez vous assurer de les retirer de QGIS d'abord.

{{% alert warning %}}

Vous ne devez pas utiliser l'option `Définir le SCR de la couche`. Cette façon de faire ne devrait être utilisée que lorsque votre couche ne s'affiche pas au bon endroit.

![](/img/img/misc/changer_projection_non.png)

{{% /alert %}}



