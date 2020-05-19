---
date: "2020-05-19" diagram: true image:   caption: "Crédit photo: [**Robert Bye**](https://unsplash.com/photos/BY34glOW7wA)"   placement: 3 math: true title: Comment structurer vos dossiers de géomatique ---
L'organisation des dossiers peut paraître un sujet futile, vous planifier gérer les données géomatiques comme vos autres dossiers client. Vous faites erreur. Les fichiers en géomatique peuvent rapidement se multiplier, et prendre énormément d’espace. Avoir une stratégie dès le départ est essentiel.
La première chose que vous devriez réfléchir est sur l’emplacement des fichiers. Les fichiers de client (plan de ferme, amas, fossé, etc.) devraient-ils être dans le dossier client? C’est assurément la méthode la plus simple. Si vous cherchez le plan de ferme d’un certain client, vous allez savoir ou le trouver. Toutefois, la notion de ce qui est propre à un client et ce qui est partagé par plusieurs peut devenir floue. Un fossé entre les champs de 2 clients devrait être dans quel dossier? Vous pourriez l’avoir dans les deux dossiers, mais si quelqu’un le modifie, il faut se souvenir d’aller le changer dans l’autre dossier. Je vous suggère donc de centraliser vos données géomatiques au même endroit. Donc d’avoir **un** shapefile de fossé, **un** d’amas, **un** de cours d’eau et **un** de plan de ferme. 

De cette façon il est beaucoup plus facile de trouver l’information que l’on cherche (mon côté machine learning vous remercie en avance...). Mais qui dit fichier centralisé, dit bonne gestion, puisqu'une erreur est si vite arrivée. Il est essentiel de faire des sauvegardes de sécurité (*backup*). Réfléchissez également à l’information qui devrait se retrouver dans chaque couche. Idéalement, l’information ne devrait pas se dédoubler, mais vous souhaitez avoir toute l’information requise à portée de main. Voici donc la structure que je suggère.
Dans un dossier que tous les utilisateurs ont accès, je mets les couches qui contiennent l'information que l'on numérise ou modifie:
img/img/misc/structure.svg)
Ensuite dans un autre dossier, je mets l'information de base, mais que l'on ne modifie pas (on pourrait mettre le dossier en lecture seule pour les plus paranos).
* Cours d'eau
* Pédologie
* Limites administratives
* Cadastre
* Index des orthophotos et du LiDAR
* Milieux humides
Finalement, je crée un dossier qui contient mes modèles autant les modèles de projet QGIS, les modèles de mise en page que les styles prédéfinis. Même si vous êtes seul à travailler avec QGIS, je vous incite à adopter une structure similaire.
Lorsqu'on doit exporter le fichier de plan de ferme pour l'importer dans le logiciel de fertilisation, je suggère de faire les jointures spatiales requises et de l'exporter dans un fichier avec la date, il s'agit d'une *photo* du plan de ferme à cette date-là.
Pour les données plus volumineuses (Orthophoto, LiDAR). Vous pouvez les avoir sur votre ordinateur. Ça va accélérer le chargement.
Le nom des fichiers devrait être suffisamment explicite. **Éviter les noms du genre test1234.shp**. Si vous souhaitez avoir une couche de test, indiquez-le clairement et supprimez-la ensuite. 
N’oubliez pas d’éviter les accents et autres caractères spéciaux dans le nom des fichiers **et des dossiers**. 