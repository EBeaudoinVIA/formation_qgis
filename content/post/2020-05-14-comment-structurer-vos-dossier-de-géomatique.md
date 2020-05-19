---
title: Comment structurer vos dossiers de géomatique
author: admin
date: '2020-05-14'
slug: comment-structurer-vos-dossier-de-géomatique
categories: []
tags: []
subtitle: ''
summary: "Cet article aborde les meilleures stratégies d'organisation de dossier et de nomenclature de fichier"
authors: []
lastmod: '2020-05-19T09:55:17-04:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---

L'organisation des dossiers peut paraître un sujet futile, vous planifier gérer les données géomatiques comme vos autres dossiers client. Vous faites erreur. Les fichiers en géomatique peuvent rapidement se multiplier, et prendre énormément d’espace. Avoir une stratégie dès le départ est essentiel.

La première chose que vous devriez réfléchir est sur l’emplacement des fichiers. Les fichiers de client (plan de ferme, amas, fossé, etc.) devraient-ils être dans le dossier client? C’est assurément la méthode la plus simple. Si vous cherchez le plan de ferme d’un certain client, vous allez savoir ou le trouver. Toutefois, la notion de ce qui est propre à un client et ce qui est partagé par plusieurs peut devenir floue. Un fossé entre les champs de 2 clients devrait être dans quel dossier? Vous pourriez l’avoir dans les deux dossiers, mais si quelqu’un le modifie, il faut se souvenir d’aller le changer dans l’autre dossier. Je vous suggère donc de centraliser vos données géomatiques au même endroit. Donc d’avoir **un** shapefile de fossé, un d’amas, un de cours d’eau et un de plan de ferme. 


De cette façon il est beaucoup plus facile de trouver l’information que l’on cherche (mon côté machine learning vous remercie en avance...). Mais qui dit fichier centralisé, dit bonne gestion, parceque'une erreur est si vite arrivée. Il est essentiel de faire des sauvegardes de sécurité (*backup*). Réfléchissez également à l’information qui devrait se retrouver dans chaque couche. Idéalement, l’information ne devrait pas se dédoubler, mais vous souhaitez avoir toute l’information requise à portée de main. Voici donc la structure que je suggère.

Dans un dossier que tous les utilisateur ont accès, je mets les couches qui contiennent l'information que l'on numérise ou modifie:

![](/img/img/misc/structure.svg)

Ensuite dans un autre dossier, je mets l'information de base, mais que l'on ne modifie pas (on pourrait mettre le dossier en lecture seule pour les plus paranos).

* Cours d'eau
* Pédologie
* Limites administratives
* Cadastre
* Index des orthophoto et du LiDAR
* Milieux humides



Finalement, je crée un dossier qui contient mes modèles autant les modèles de projet QGIS, les modèles de mise en page que les styles prédéfini. Même si vous êtes seul à travailler avec QGIS, je vous incite à adopter une structure similaire.


Pour les données plus volumineuses (Orthophoto, LiDAR). Vous pouvez les avoir sur votre ordinateur. Ça va accélérer le chargement.

Le nom des fichiers devrait être suffisamment explicite. **Éviter les test1234.shp**. Si vous souhaitez avoir une couche de test, indiquez-le clairement et supprimez-la ensuite. 

N’oubliez pas d’éviter les accents et autres caractères spéciaux dans le nom des fichiers **et des dossiers**. 



