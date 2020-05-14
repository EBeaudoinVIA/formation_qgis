---
date: "2019-05-05T00:00:00+01:00"
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

Toutes les sessions d’édition commencent par le choix de l’option toggleEditing Basculer en mode édition que l’on trouve dans le menu contextuel de la couche en question, dans la boîte de dialogue de la table d’attributs, dans la barre d’outils de numérisation ou encore dans le menu Éditer.


Une fois que la couche est en mode d’édition, des boutons d’outils supplémentaires dans la barre d’outils d’édition sont disponibles et des symboles apparaissent aux sommets de toutes les entités.

En général, les outils d’édition des couches vectorielles sont divisés en une barre d’outils de numérisation et une barre d’outils de numérisation avancée,

## Modifier les noeuds

Pour toute couche vectorielle éditable, l’outil vertexToolActiveLayer outil de noeud (couche courante) fournit des capacités de manipulation des sommets d’entités similaires aux programmes de CAO. Il est possible de sélectionner simplement plusieurs sommets à la fois et de les déplacer, les ajouter ou les supprimer complètement. L’outil sommet prend également en charge la fonction d’édition topologique. Cet outil est une sélection persistante, donc quand une opération est effectuée, la sélection reste active pour cette entité et cet outil.

* Sélection de sommets : Vous pouvez sélectionner des sommets en cliquant dessus un par un en maintenant Shift enfoncée, ou en cliquant et en faisant glisser un rectangle autour de certains sommets. Lorsqu’un sommet est sélectionné, sa couleur devient bleue. Pour ajouter plus de sommets à la sélection actuelle, maintenez la touche Shift enfoncée tout en cliquant. Pour supprimer des sommets de la sélection, maintenez enfoncée la touche Ctrl.


* Ajout de sommets: pour ajouter un sommet, un nouveau nœud virtuel apparaît au centre du segment. Saisissez-le simplement pour ajouter un nouveau sommet. Un double-clic sur n’importe quel emplacement de la limite crée également un nouveau nœud. Pour les lignes, un nœud virtuel est également proposé aux deux extrémités d’une ligne pour l’étendre.



* Suppression de sommets: Sélectionnez les sommets et cliquez sur la touche Supprimer. La suppression de tous les sommets d’une entité génère, si elle est compatible avec la source de données, une entité sans géométrie. Notez que cela ne supprime pas la fonction complète, juste la pièce géométrique. Pour supprimer une entité complètement, utilisez la commande deleteSelectedFeatures :sup: »Supprimer la sélection ».

* Déplacement des sommets: sélectionnez tous les sommets que vous souhaitez déplacer, cliquez sur un sommet ou une arête sélectionnée, puis cliquez à nouveau sur le nouvel emplacement souhaité. Tous les sommets sélectionnés se déplaceront ensemble. 

1. Démarrer le mode édition
1. Sélectionner l'outil de modification de noeuds
1. Sélectionner le noeud à modifier ou double cliquer entre 2 noeuds pour en ajouter un
1. Cliquer sur l'endroit où on veut mettre le noeud
1. Enregistrer
1. Arrêter le mode édition


![](/img/gif/mod_noeuds.gif)


## Découper

Utilisez l’outil splitFeatures Séparer entités pour diviser une entité en deux ou plusieurs nouvelles entités indépendantes, c’est-à-dire. chaque géométrie correspondant à une nouvelle ligne dans la table attributaire.

Pour couper des entités linéaires ou surfaciques:

Sélectionnez l’outil splitFeatures séparer entités.

Tracez une ligne sur la ou les entités que vous souhaitez couper. Si une sélection est active, seules les entités sélectionnées sont coupées. Lorsqu’elles sont définies, les valeurs par défaut et contraintes sont appliquées aux champs correspondants et les autres attributs de l’entité parent sont copiés par défaut dans les nouvelles entités.

Vous pouvez ensuite, comme d’habitude, modifier l’un des attributs de toute entité résultante.

1. Démarrer le mode édition
1. Sélectionner l'outil de découpage
1. Commencer le découpage en dehors de l'entité
1. Finir le découpage en dehors de l'entité
1. Clique droit pour terminer
1. Enregistrer
1. Arrêter le mode édition


![](/img/gif/couper.gif)

## Fusionner

L’outil mergeFeatures Fusionner les entités sélectionnées permet de créer une nouvelle entité à partir d’entités existantes: sa géométrie est le résultat de la fusion des géométries de départ. Si les entités n’ont pas de frontière commune alors un multi-polygone/multiligne/multipoint sera créé.

Tout d’abord, sélectionnez les entités que vous souhaitez combiner.

Appuyez ensuite sur le bouton fusionner les entités sélectionnées.

Dans la nouvelle boîte de dialogue, la ligne :guilabel:`fusionner`en bas du tableau affiche les attributs de l’entité résultante. Vous pouvez modifier l’une de ces valeurs en:

remplacer manuellement la valeur dans la cellule correspondante;

sélectionner une ligne dans le tableau et appuyer sur Récupérer les attributs de l’entité sélectionnée pour utiliser les valeurs de cette entité initiale;

en appuyant sur Ignorer tous les attributs pour utiliser des attributs vides;


1. Démarrer le mode édition
1. Sélectionner les entité à fusionner (lignes et polygones)
1. Cliquer sur l'outil de fusion
1. Saisir l'information
1. Enregistrer
1. Arrêter le mode édition



![](/img/gif/fusion.gif)

