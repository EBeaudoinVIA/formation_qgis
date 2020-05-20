---
date: "2020-05-19T00:00:00+01:00"
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

Les projections sont un sujet complexe : même des professionnels qui ont étudié la géographie ou d’autres sciences liées aux SIG ont souvent des problèmes à bien définir les projections et les systèmes de coordonnées de référence (SCR). Cela dit, c’est toujours utile d’avoir une idée de ce que signifient une projection de carte et un SCR.




## Coordonnées



Les lignes de latitude courent parallèlement à l’équateur et divisent la terre en 180 sections séparées de manière égale du Nord au Sud (ou du Sud au Nord). La ligne de référence pour la latitude est l’équateur et chaque hémisphère est divisé en quatre-vingt-dix sections, chacune représentant un degré de latitude. Dans l’hémisphère Nord, les degrés de latitude sont mesurés depuis zéro à l’équateur jusqu’à quatre-vingt-dix au pôle Nord. Dans l’hémisphère Sud, les degrés de latitude sont mesurés depuis zéro à l’équateur jusqu’à quatre-vingt-dix au pôle Sud. Pour simplifier la numérisation des cartes, les degrés de latitude dans l’hémisphère Sud sont souvent assignés à des valeurs négatives (0 à -90°). Peu importe où vous vous trouvez sur la surface terrestre, la distance entre les lignes de latitude est la même (60 miles nautiques).


Les lignes de longitude, d’autre part, ne résistent pas aussi bien à la norme d’uniformité. Les lignes de longitude courent perpendiculairement à l’équateur et convergent aux pôles. La ligne de référence pour la longitude (le méridien) court du pôle Nord au pôle Sud via Greenwich, Angleterre. Les lignes ultérieures de longitude sont mesurées depuis zéro jusqu’à 180 degrés à l’Est ou à l’Ouest du méridien. Notez que les valeurs à l’Ouest du méridien sont assignées à des valeurs négatives.

À l’équateur, et seulement à l’équateur, la distance représentée par une ligne de longitude est égale à la distance représentée par un degré de latitude. Lorsque vous vous déplacez vers les pôles, la distance entre les lignes de longitude devient progressivement moins grande, jusqu’à ce que, à l’exacte position du pôle, les 360° de longitude soient représentés par un unique point sur lequel vous pouvez mettre votre doigt. 

Les degrés sont divisés en minutes (') et secondes ("). Il y a soixante minutes dans un degré, et soixante secondes dans une minute (3600 secondes dans un degré). Donc, à l’équateur, une seconde de latitude ou de longitude égale 30.87624 mètres. Les coordonnées peuvent également être exprimées en degrés décimaux. 


![](/img/img/misc/dms2dd.png)





## Projections




Lorsque l’on voit la terre depuis la terre, elle semble être plate. Cependant, lorsqu’on la regarde depuis l’espace, on constate qu’elle est sphérique. Les cartes ne servent pas juste à représenter les apparences, mais aussi les formes et les dispositions géographiques. Chaque projection cartographique a des avantages et des désavantages. La meilleure projection d’une carte dépend de l’échelle de la carte et de l’objectif pour laquelle elle sera utilisée. Par exemple, une projection peut avoir des distorsions inacceptables si elles sont utilisées pour cartographier l’ensemble du continent africain, mais peut être un excellent choix pour une carte à grande échelle (détaillée) de votre pays. Les propriétés d’une projection cartographique peuvent aussi influencer certaines caractéristiques de conception de la carte. Certaines projections sont bonnes pour de petites zones, d’autres pour cartographier une large étendue Est-Ouest et d’autres sont bonnes pour cartographier des zones avec une grande étendue Nord-Sud.


{{< youtube kIID5FDi2JQ >}}



Les projections cartographiques ne sont jamais une représentation absolument exacte de la Terre. À chaque projection, les cartes affichent des distorsions sur la conformité des angles, des distances et des surfaces. Une projection cartographique peut combiner plusieurs de ces caractéristiques, ou peut être un compromis entre ces déformations de surfaces, de distances et d’angles, dans des limites raisonnables.

![](/img/img/misc/bad_map_projection.png)


Pour définir la projection, on définit en premier la forme de la Terre (Datum), puis la projection qui sert à la mettre en 2 dimensions. Pour simplifier la gestion des projections, il existe un registre où chaque projection possède un code numérique à 4 ou 5 chiffres. 


![](/img/img/misc/epsg.png)



## Utilisation en agronomie

Pour l'usage du conseiller agricole, le choix de la projection n'est généralement pas crucial. De nombreuses projections sont adéquates pour représenter les parcelles agricoles avec seulement de légères différences dans les évaluations de surfaces ou de distances.

![](/img/img/misc/sup_projection.png)

Dans les SIG, il y a une fonctionnalité appelée *projection à la volée*. Cette fonctionnalité reprojette automatiquement vos couches afin qu’elles soient visibles sur la carte. Donc, il est possible de travailler avec des couches ayant différentes projections. Toutefois, il est important de noter que l'analyse spatiale impliquant des couches projetées différemment est impossible. Donc, il est fortement recommandé d'avoir toutes ses couches dans la même projection.

Au Québec, la Financière agricole utilise la projection *EPSG: 6622 - NAD 83 | Québec Lambert* pour les plans de ferme. Comme cette projection est valable pour tout le territoire du Québec, je vous suggère de l'utiliser.





