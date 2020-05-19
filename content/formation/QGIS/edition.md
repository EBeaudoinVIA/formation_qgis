---
date: "2020-05-19T00:00:00+01:00"
draft: false
linktitle: Édition
menu:
  example:
    parent: QGIS
    weight: 6
title: Édition
toc: true
type: docs
weight: 6
---

Par défaut, QGIS charge les couches en lecture seule : c’est une sécurité pour éviter d’éditer accidentellement une couche. 

Toutes les sessions d’édition commencent en cliquant sur le crayon que l’on trouve dans le menu contextuel de la couche en question, dans la boîte de dialogue de la table d’attributs, dans la barre d’outils de numérisation ou encore dans le menu Éditer.


Une fois que la couche est en mode d’édition, des boutons d’outils supplémentaires dans la barre d’outils d’édition sont disponibles et des symboles apparaissent aux sommets de toutes les entités.

En général, les outils d’édition des couches vectorielles sont divisés en une barre d’outils de numérisation et une barre d’outils de numérisation avancée.

## Modifier les noeuds

Pour toute couche vectorielle éditable, l’outil de noeud fournit des capacités de manipulation des sommets d’entités similaires aux programmes de dessins assistés par ordinateur (DAO). Il est possible de sélectionner simplement plusieurs sommets à la fois et de les déplacer, les ajouter ou les supprimer complètement.

* Sélection de sommets : Vous pouvez sélectionner des sommets en cliquant dessus un par un en maintenant Shift enfoncée, ou en cliquant et en faisant glisser un rectangle autour de certains sommets. Lorsqu’un sommet est sélectionné, sa couleur devient bleue. Pour ajouter plus de sommets à la sélection actuelle, maintenez la touche Shift enfoncée tout en cliquant. Pour supprimer des sommets de la sélection, maintenez enfoncée la touche Ctrl.


* Ajout de sommets: un nouveau nœud virtuel apparaît au centre du segment. Saisissez-le simplement pour ajouter un nouveau sommet. Un double-clic sur n’importe quel emplacement de la limite crée également un nouveau nœud. Pour les lignes, un nœud virtuel est également proposé aux deux extrémités d’une ligne pour l’étendre.



* Suppression de sommets: Sélectionnez les sommets et cliquez sur la touche Supprimer. 

* Déplacement des sommets: sélectionnez tous les sommets que vous souhaitez déplacer, cliquez sur un sommet ou une arête sélectionnée, puis cliquez à nouveau sur le nouvel emplacement souhaité. Tous les sommets sélectionnés se déplaceront ensemble. 



{{< figure library="true" src="gif/mod_noeuds.gif" title="Modifier les noeuds" lightbox="true" >}}

## Découper

Utilisez l’outil  `Séparer entités` pour diviser une entité en deux ou plusieurs nouvelles entités indépendantes, c’est-à-dire. chaque géométrie correspondant à une nouvelle ligne dans la table attributaire.


Tracez une ligne sur la ou les entités que vous souhaitez couper. La ligne doit dépasser l'entité que vous souhaitez couper. Si une sélection est active, seules les entités sélectionnées sont coupées.

Vous pouvez ensuite, comme d’habitude, modifier l’un des attributs de toute entité résultante.

1. Démarrer le mode édition
1. Sélectionner l'outil de découpage
1. Commencer le découpage en dehors de l'entité
1. Finir le découpage en dehors de l'entité
1. Clique droit pour terminer
1. Enregistrer
1. Arrêter le mode édition



{{< figure library="true" src="gif/couper.gif" title="Découper" lightbox="true" >}}

## Fusionner

L’outil `Fusionner les entités sélectionnées` permet de créer une nouvelle entité à partir d’entités existantes: sa géométrie est le résultat de la fusion des géométries de départ. Si les entités n’ont pas de frontière commune alors un multi-polygone/multiligne/multipoint sera créé.

Si vous souhaitez fusionner des parcelles agricoles, assurez-vous que les limites des parcelles se recoupent.

Tout d’abord, sélectionnez les entités que vous souhaitez combiner.

Appuyez ensuite sur le bouton fusionner les entités sélectionnées.

Dans la nouvelle boîte de dialogue, la ligne `fusionner` en bas du tableau affiche les attributs de l’entité résultante. Vous pouvez modifier l’une de ces valeurs en:

remplacer manuellement la valeur dans la cellule correspondante;

sélectionner une ligne dans le tableau et appuyer sur Récupérer les attributs de l’entité sélectionnée pour utiliser les valeurs de cette entité initiale;

en appuyant sur Ignorer tous les attributs pour utiliser des attributs vides;




{{< figure library="true" src="gif/fusion.gif" title="Fusionner" lightbox="true" >}}