---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Projections
menu:
  example:
    parent: Principes de base
    weight: 1
title: Projections
toc: true
type: docs
weight: 1
---


Lorsque l’on voit la terre depuis la terre, elle semble être plate. Cependant, lorsqu’on la regarde depuis l’espace, on constate qu’elle est sphérique. Les cartes, comme nous le verrons dans le prochain sujet de production de cartes, sont des représentations de la réalité. Elles ne servent pas juste à représenter les apparences, mais aussi les formes et les dispositions géographiques. Chaque projection cartographique a des avantages et des désavantages. La meilleure projection d’une carte dépend de l’échelle de la carte, et pour l’objectif pour laquelle elle sera utilisée. Par exemple, une projection peut avoir des distorsions inacceptables si elles sont utilisées pour cartographier l’ensemble du continent africain, mais peut être un excellent choix pour une carte à grande échelle (détaillée) de votre pays. Les propriétés d’une projection cartographique peuvent aussi influencer certaines caractéristiques de conception de la carte. Certaines projections sont bonnes pour de petites zones, d’autres pour cartographier une large étendue Est-Ouest et d’autres sont bonnes pour cartographier des zones avec une grande étendue Nord-Sud.


{{< youtube kIID5FDi2JQ >}}



Les projections cartographiques ne sont jamais une représentation absolument exacte de la Terre. À chaque projection, les cartes affichent des distorsions sur la conformité des angles, des distances et des surfaces. Une projection cartographique peut combiner plusieurs de ces caractéristiques, ou peut être un compromis entre ces déformations de surface, de distance et d’angle, dans des limites raisonnables.

Grâce aux systèmes de coordonnées de référence (SCR), chaque point de la terre peut être spécifié par un ensemble de trois nombres, appelé coordonnées. En général, les SCR se divisent en systèmes de coordonnées de référence projetés (aussi appelés systèmes de coordonnées de référence cartésiens ou rectangulaires) et systèmes de coordonnées de référence géographique.
L’utilisation des Systèmes de Coordonnées Géographique est très courante. Pour définir un point à la surface de la Terre, ils utilisent la Latitude et la Longitude qui s’expriment en degrés, et parfois une valeur de hauteur est donnée en plus. Le plus connu et le plus utilisé est le WGS 84.

Les Lignes de latitude courent parallèlement à l’équateur et divisent la terre en 180 sections séparées de manière égale du Nord au Sud (ou du Sud au Nord). La ligne de référence pour la latitude est l’équateur et chaque hémisphère est divisé en quatre-vingt-dix sections, chacune représentant un degré de latitude. Dans l’hémisphère nord, les degrés de latitude sont mesurés depuis zéro à l’équateur jusqu’à quatre-vingt-dix au pôle nord. Dans l’hémisphère sud, les degrés de latitude sont mesurés depuis zéro à l’équateur jusqu’à quatre-vingt-dix au pôle sud. Pour simplifier la numérisation des cartes, les degrés de latitude dans l’hémisphère sud sont souvent assignés à des valeurs négatives (0 à -90°). Peu importe où vous vous trouvez sur la surface terrestre, la distance entre les lignes de latitude est la même (60 miles nautiques).
Les Lignes de longitude, d’autre part, ne résistent pas aussi bien à la norme d’uniformité. Les lignes de longitude courent perpendiculairement à l’équateur et convergent aux pôles. La ligne de référence pour la longitude (le méridien) court du Pôle Nord au Pôle Sud via Greenwich, Angleterre. Les lignes ultérieures de longitude sont mesurées depuis zéro jusqu’à 180 degrés à l’Est ou à l’Ouest du méridien. Notez que les valeurs à l’Ouest du méridien sont assignées à des valeurs négatives à utiliser dans des applications de cartographie digitale.

À l’équateur, et seulement à l’équateur, la distance représentée par une ligne de longitude est égale à la distance représentée par un degré de latitude. Lorsque vous vous déplacez vers les pôles, la distance entre les lignes de longitude devient progressivement moins grande, jusqu’à ce que, à l’exacte position du pôle, les 360° de longitude soient représentés par un unique point sur lequel vous pouvez mettre votre doigt (même si vous auriez probablement envie de porter des gants). En utilisant le système de coordonnées géographiques, nous avons une grille de lignes divisant la terre en carrés qui couvrent approximativement 12363.365 kilomètres carrés à l’équateur — un bon départ, mais pas très utile pour déterminer la localisation de n’importe quoi d’autre sans ce carré.
Pour être vraiment utile, une grille de carte doit être divisée en suffisamment de petites sections de sorte qu’elles puissent être utilisées pour décrire (avec un niveau acceptable de précision) l’emplacement d’un point sur la carte. Pour faire ceci, les degrés sont divisés en minutes (') et secondes ("). Il y a soixante minutes dans un degré, et soixante secondes dans une minute (3600 secondes dans un degré). Donc, à l’équateur, une seconde de latitude ou de longitude = 30.87624 mètres.

Le sujet projection de la carte est très complexe et même des professionnels qui ont étudié la géographie, la géodésie et toutes autres sciences liées aux SIG ont souvent des problèmes avec la définition correcte des projections de cartes et les systèmes de coordonnées de référence. Habituellement, lorsque vous travaillez avec des SIG, vous avez déjà projeté les données pour commencer. Dans la plupart des cas, ces données seront projetées dans un certain SCR, donc vous n’avez pas besoin de créer un nouveau SCR ou même de reprojeter les données d’un SCR à un autre. Cela dit, c’est toujours utile d’avoir une idée sur ce que signifient une projection de carte et un SCR.

Les « Projections de Cartes » figurent la surface de la Terre sur une représentation à deux dimensions, sur une feuille de papier ou sur un écran d’ordinateur.

Il existe des projections « globales », mais la plupart des projections sont adaptées à une représentation de petites zones par rapport à la surface de la Terre.

Les Projections ne donnent jamais une représentation exacte de la rotondité de la terre. « La conformité des angles, des distances et des surfaces » n’est pas toujours respectée. C’est d’ailleurs impossible de respecter toutes ces caractéristiques mathématiques à la fois sur une projection.

Un « Système de Coordonnées de Référence » (SCR) définit, avec l’aide des coordonnées, comment des lieux réels sur terre sont projetés sur un plan à deux dimensions.

Il y a deux types de systèmes de coordonnées de référence : Systèmes de Coordonnées géographiques et Systèmes de Coordonnées projetées.

La projection à la volée est une fonctionnalité dans les SIG qui permet de superposer des couches, même si elles sont projetées dans différents systèmes de coordonnées de référence.

![](/img/img/misc/epsg.png)

![](/img/img/misc/sup_projection.png)

![](/img/img/misc/bad_map_projection.png)