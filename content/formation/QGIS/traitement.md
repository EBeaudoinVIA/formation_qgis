---
date: "2020-05-19T00:00:00+01:00"
draft: false
linktitle: Traitement
menu:
  example:
    parent: QGIS
    weight: 9
title: Traitement
toc: true
type: docs
weight: 9
---

L'analyse spatiale est le processus de manipulation de l’information spatiale pour en extraire une nouvelle information ou l’interprétation des données originelles.

La façon la plus simple de trouver l'algorithme que l'on cherche est souvent d'effectuer une recherche. Dans la boîte Recherche, vous pouvez saisir n’importe quel mot ou expression (en anglais ou en français) dans la zone de texte. Notez que, lorsque vous tapez, le nombre d’algorithmes, de modèles ou de scripts dans la boîte à outils est réduit à ceux qui contiennent le texte que vous avez entré dans leurs noms ou mots clés.

Il arrive fréquemment qu'un algorithme ne permette pas de réaliser ce que l'on souhaite, il faut à ce moment souvent décomposer le problème et y aller une étape à la fois.

## Ouvrir la boîte à outils

Il est possible que le panneau de boîte à outils ne soit pas présent au démarrage de QGIS. Pour l'ouvrir, cliquez sur l'icône:

![](/img/img/bouton/processingAlgorithm.png.png)

{{< figure library="true" src="gif/ouvrir_boite_outils.gif" title="Ouvrir la boîte à outils" lightbox="true" >}}


Pour démarrer un algorithme, double-cliquez sur l'algorithme de votre choix. Une fenêtre ouvrira et vous devrez sélectionner les options appropriées.



## Tampon

La création de tampons créée généralement deux surfaces: l’une à l’intérieur d’une distance paramétrée des entités, l’autre, à l’extérieur. La surface qui est à l’intérieur de la distance est appelée zone tampon.

Dans une application SIG, les zones tampons sont toujours représentées comme des polygones vectoriels qui entourent d’autres polygones, lignes ou points.

Dans QGIS, l'outil de base `Tampon` fonctionne bien. Il se trouve dans le menu de `Géométrie vectorielle`. Pour les besoins de base, vous pouvez seulement choisir la couche et indiquer la largeur du tampon désiré en mètre. La couche créée par l’algorithme est par défaut en mémoire temporaire.


{{< figure library="true" src="gif/tampon.gif" title="Tampon" lightbox="true" >}}

## Tampon négatif

Les zones tampon autour des entités polygones sont généralement étendues vers l’extérieur des limites du polygone. Mais il est également possible de créer des zones tampons à l’intérieur.

Dans QGIS, vous pouvez encore utiliser l’outil `Tampon` en utilisant une valeur négative.

{{< figure library="true" src="gif/tampon_negatif.gif" title="Tampon négatif" lightbox="true" >}}

## Refactoriser

Refactoriser est un terme **fancy** pour signifier changer les colonnes dans la table attributaire. Dans QGIS, l’outil se nomme `Refactorise les champs` et se trouve dans le menu `Table vecteur`. Il permet de changer l’ordre des colonnes ou les noms de colonnes. L’outil permet également de charger une autre couche comme référence. C’est particulièrement utile pour renommer toutes les colonnes d’une couche afin qu’elles soient pareilles.


{{< figure library="true" src="gif/refactoriser.gif" title="Refactoriser" lightbox="true" >}}





## Jointure

Il est assez fréquent qu’on souhaite extraire l’information d’une couche selon sa localisation. Par exemple, extraire la série de sols par champ. La façon la plus simple est d’utiliser l’outil `Joindre les attributs par localisation` dans le menu `Outils généraux pour les vecteurs`. 


{{< figure library="true" src="gif/jointure_simple.gif" title="Requêtes (entre différentes couches)" lightbox="true" >}}

{{% alert warning %}}

Lorsque vous utilisez cet outil, il ne prend que la première jonction. Par exemple, si j’ai un champ qui se trouve dans deux villes, il va prendre la première ville qu’il croise et non celle qui occupe la plus grande proportion du champ.

{{< figure library="true" src="gif/jointure_erreur.gif" title="Requêtes (entre différentes couches)" lightbox="true" >}}


{{% /alert %}}


Si on veut obtenir toutes les intersections, on peut utiliser l’outil `Intersection` dans le menu `Recouvrement de vecteur`. Il crée alors une couche qui combine l’information des deux couches.

Si l’on souhaite obtenir l’information qui se retrouve majoritairement sous le polygone (par exemple, série de sol dominante), on procède ainsi:

1. On fait l’intersection entre la couche de champ et celle contenant l’information avec l’outil `Intersection`.
1. On trie la couche d’intersection selon la superficie à l’aide de l’outil `Ordonner par expression`.
1. On supprime les doublons en indiquant le nom d’une colonne qui contient de l’information unique sur chaque entité (par exemple le numéro de champ) `Supprimer les doublons par attributs`.
1. On a alors une couche d’intersections qui ne contient que le polygone le plus grand pour chaque champ.
1. On peut ensuite joindre l’information soit comme on l’a vu précédemment `Joindre les attributs par localisation` ou en joignant l’information à l’aide du numéro de champ `Joindre les attributs par valeur de champs`.

{{< figure library="true" src="gif/jointure_superficie.gif" title="Requêtes (entre différentes couches)" lightbox="true" >}}


{{% alert note %}}

Pour ceux qui trouvent que cette procédure est trop exigeante, il est possible d’automatiser des tâches dans QGIS. Vous pouvez consulter l’article https://formation-qgis.netlify.app/post/modele/ qui aborde exactement ce sujet-là.

{{% /alert %}}





