---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Sources de données
menu:
  example:
    parent: QGIS
    weight: 11
title: Sources de données
toc: true
type: docs
weight: 11
---


## [Données Québec](https://www.donneesquebec.ca/recherche/fr/dataset?sort=metadata_created+desc&res_format=SHP)




Depuis quelques années, le gouvernement du Québec fournit des données de base gratuitement en ligne. C'est une bonne place pour commencer ses recherches.

Voici les couches que je trouve particulièrement utiles.

* [Cours d'eau](https://www.donneesquebec.ca/recherche/fr/dataset/grhq)

* [Limites administratives](https://www.donneesquebec.ca/recherche/fr/dataset/decoupages-administratifs) 

* [Zone agricole](https://www.donneesquebec.ca/recherche/fr/dataset/zone-agricole-du-quebec)

* [Milieux humides](https://www.donneesquebec.ca/recherche/fr/dataset/milieux-humides-du-quebec)  


## [Financière agricole](https://www.donneesquebec.ca/recherche/fr/organization/fadq)

* [Centres et comptoirs de services de La Financière agricole](https://www.donneesquebec.ca/recherche/fr/dataset/centres-et-comptoirs-de-services-de-la-financiere-agricole-du-quebec)
* [Territoires des stations météo](https://www.donneesquebec.ca/recherche/fr/dataset/territoires-des-stations-meteo)
* [Zonage système collectif céréales et maïs fourrager](https://www.donneesquebec.ca/recherche/fr/dataset/zonage-systeme-collectif-cereales-et-mais-fourrager)
* [Zonage système collectif maïs-grain](https://www.donneesquebec.ca/recherche/fr/dataset/zonage-systeme-collectif-mais-grain)


* [Base de données des parcelles et productions agricoles déclarées](https://www.donneesquebec.ca/recherche/fr/dataset/base-de-donnees-des-parcelles-et-productions-agricoles-declarees-bdppad)




## WMS / WFS


Un Web Mapping Service (WMS, qui signifie Service de cartographie web en anglais) est un service hébergé sur un serveur distant. Semblable à un site web, vous pouvez y accéder tant que vous avez une connexion au serveur. En utilisant QIGS, vous pouvez charger un répertoire WMS directement dans votre carte existante.

Vous devez vous souvenir de la leçon sur les extensions qu’il est possible de charger une nouvelle image raster depuis Google, par exemple. Cependant, il s’agit d’une transaction ponctuelle : une fois que vous avez téléchargé l’image, elle ne change pas. Un WMS est différent dans le fait que c’est un service en direct qui actualisera automatiquement sa vue si vous déplacez ou zoomez sur la carte.

Un Web Feature Service (WFS) fournit à ses utilisateurs des données SIG dans des formats qui peuvent être directement chargés dans QGIS. À la différence d’un WMS, qui vous fournit seulement une carte que vous ne pouvez pas modifier, un WFS vous donne accès aux entités elles-mêmes.

Un service de WFS retourne la couche en elle-même et pas uniquement une carte rendue avec. Cela vous donne un accès direct à la donnée et signifie que vous pouvez changer sa symbologie et lancer des fonctions d’analyse dessus. Néanmoins, cela se fait en transmettant beaucoup plus de données. Cela se révélera particulièrement inadapté si les couches que vous chargez ont des formes complexes, un grand nombre d’attributs ou de nombreuses entités ou encore si vous chargez un grand nombre de couches. Les couches WFS prennent un temps non négligeable à se charger à cause de tout cela.


Les gouvernements sont une source intéressante de données WMS et WFS. Voici une liste de serveur avec les couches disponible.

| Type       | URL                                                                                                 | Couches                                                                                               |
|----------- |---------------------------------------------------------------------------------------------------- |------------------------------------------------------------------------------------------------------ |
| WMS        | https://servicescarto.mern.gouv.qc.ca/pes/services/Territoire/AQreseauPlus_WMS/MapServer/WMSServer  | Réseau routier<br>Aéroport                                                                            |
| WMS<br>WFS  | https://carto.cptaq.gouv.qc.ca/cgi-bin/cptaq                                                        | Zone agricole<br>Décisions<br>Inclusion - Exclusion                                                   |
| WMS<br>WFS  | https://carto.cptaq.gouv.qc.ca/cgi-bin/cptaq_igo                                                    | Zone agricole<br>Potentiel ARDA<br>Potentiel acéricole<br>Municipalité<br>Adresse<br>Cadastre rénové  |
| WMS        | https://geoegl.msp.gouv.qc.ca/ws/bdga.fcgi                                                          | Ville<br>Région<br>MRC<br>Routes<br>Électricité<br>Rivières                                           |
| WMS        | https://servicesmatriciels.mern.gouv.qc.ca/erdas-iws/ogc/wms/Cartes_Images                          | Fond de carte                                                                                         |
| WMS        | https://geo.weather.gc.ca/geomet/?lang=F                                                            | Météo                                                                                                 |
| WMS        | https://maps.ducks.ca/arcgis/services/Public/QC_Carto_MH_sudqc_mai2019/MapServer/WMSServer          | Milieux humides                                                                                       |
| WMS<br>WFS  | https://geoegl.msp.gouv.qc.ca/ws/mffpecofor.fcgi?                                                   | Données écoforestières<br>Téléchargement de LiDAR<br>                                                 |

