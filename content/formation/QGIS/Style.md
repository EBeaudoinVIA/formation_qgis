---
date: "2020-05-19T00:00:00+01:00"
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

Lorsqu’une couche est ajoutée au canevas de carte, QGIS utilise un symbole/couleur aléatoire pour le rendu de ses entités. Vous pouvez néanmoins paramétrer un symbole par défaut dans Projet –> Propriétés –> Styles par défaut qui sera appliqué à chaque nouvel ajout de couche selon le type géométrique de cette dernière.

Cependant, la plupart du temps, vous voudrez disposer d’un style plus complexe et plus personnalisé 



## Symbologie

Si une entité est symbolisée sans utiliser les données de la table attributaire, elle peut seulement être symbolisée d’une façon simple. Par exemple avec des entités de point, vous pouvez configurer la couleur et le symbole (cercle, carré, étoile, etc.), mais c’est tout. 

Un symbole peut consister en plusieurs couches de symbole superposé avec des formes, des couleurs, des tailles et des niveaux de transparence différents.



## Définir la symbologie

Pour définir la symbologie, on clique droit sur une couche puis on sélectionne `Propriétés...`. On peut également double cliquer sur la couche.

Ensuite on sélectionne l'onglet `Contrôle la symbologie de l'entité`.

![](/img/img/bouton/symbology.png)

Dans cet onglet où peut soit sélectionner un style préenregistré ou créer un nouveau style.


{{< figure library="true" src="gif/symbologie.gif" title="Définir la symbologie" lightbox="true" >}}

## Symbologie par catégorie




On peut également faire varier la symbologie selon une colonne de la table attributaire. On peut soit assigner un style pour chaque valeur unique dans la table (par exemple avoir un style pour les parcelles louées et un pour les parcelles que le client possède) ou avoir un style qui varie selon un attribut numérique (changer la couleur selon la superficie d'une parcelle).

Dans l'onglet `Contrôle la symbologie de l'entité`, il suffit de  remplacer `Symbole unique` par `Catégorisé` ou `Gradué` dans le menu déroulant situé dans le haut.



{{< figure library="true" src="gif/symbologie_categorie.gif" title="Symbologie par catégorie" lightbox="true" >}}


## Étiquettes

Dans la fenêtre `Propriété de la couche` on peut également ajouter des étiquettes aux entités. Il suffit de cliquer sur l'onglet `Contrôle l'étiquetage des entités`

![](/img/img/bouton/labelingSingle.png)

Dans le menu déroulant du haut, sélectionner `Étiquettes simples`, puis de la barre valeur choisissez un attribut ou saisissez une formule. Les options contenues dans cet onglet permettent de changer la police, l'arrière-plan, la position, l'orientation et la visibilité des étiquettes selon l'échelle. 


{{< figure library="true" src="gif/etiquette.gif" title="Étiquettes" lightbox="true" >}}

## Enregistrer un style

Définir un "beau" style peut prendre du temps, et il est souvent souhaitable d'établir des styles qu'on réutilise d'une fois à l'autre pour le même type d'information. Par exemple, tous les puits ont le même symbole. Il est donc utile d'enregistrer les styles dans un fichier et de se les partager. Lorsque vous enregistrez un projet, vous enregistrez la symbologie, mais si vous partez d'un projet vide, il peut être utile d'avoir le fichier de style.


{{< figure library="true" src="gif/save_style.gif" title="Enregistrer un style" lightbox="true" >}}

{{% alert note %}}

Enregistrer le symbole n'est pas la même chose qu'enregistrer le style. Enregistrer le symbole signifie que vous allez conserver votre symbologie (la couleur du polygone, le type de ligne, etc.) dans vos styles enregistrés dans QGIS. Enregistrer le style enregistre à la fois le symbole, mais aussi les étiquettes dans un fichier séparé.

{{< figure library="true" src="gif/save_symbole.gif" title="Enregistrer un symbole" lightbox="true" >}}

{{% /alert %}}









