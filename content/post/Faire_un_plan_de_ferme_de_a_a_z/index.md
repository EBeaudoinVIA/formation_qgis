---
date: "2020-06-19"
diagram: true
image:
  caption: "Crédit photo: [**Annie Spratt**](https://unsplash.com/photos/AFB6S2kibuk)"
  placement: 3
math: true
numbersections: true
title: Faire un plan de ferme en 15 étapes
---

Voici la procédure simple pour faire un plan de ferme pour un nouveau client et de calculer la superficie épandable.

## 1. Téléchargez le projet démo

Pour faciliter votre travail dans QGIS, nous avons préparé des projets pré-configurés, contenant les couches d'informations requises, des styles et des mises en page prédéfinies. Nous vous invitons à télécharger un des modèles divisés par région administrative ci-dessous. 





<iframe src="https://drive.google.com/embeddedfolderview?id=1XXKXesdTfglVrqOAHMuY6uvCyp07pcso#list" width="100%" height="500" frameborder="0"title=”Projet démo par région administrative"></iframe>






{{< figure library="true" src="gif/telecharger_modele.gif" title="Téléchargez un modèle" lightbox="true" >}}





## 2. Dézippez le projet démo

Avant de travailler avec le projet, il faut le dézipper. Cliquer droit sur le fichier téléchargé puis faites extraire tout.



{{< figure library="true" src="gif/dezip.gif" title="Dézippez le fichier" lightbox="true" >}}


## 3. Dupliquez le client démo et Ouvrez le projet

Une fois dézippé, on clique sur le dossier "client_demo", puis on fait copier-coller pour le dupliquer. On le renomme avec le nom de notre client.Dans le dossier nouvellement créer, on renomme le projet "client_demo.qgz" pour le nom de notre client. Ensuite on double-clique dessus pour l'ouvrir. 


Lorsqu'on place le dossier client_demo à l'endroit approprié, QGIS va demandé où se trouvent les données. Il suffit de remplacer le nom du dossier par le nom du dossier où se trouvent les données dontenue dans le dossier commun.




## 4. Description du projet

Dans le projet qu'on vient d'ouvrir, nous avons déjà ajouté plusieurs couches. Voici la liste des couches ainsi qu'une brève description.

### Sous-groupe Client

|  Couche|  Description|
|--:|--:|
|  plan de ferme|  Couche contenant le contour des champs ainsi que l'information requise pour le logiciel de fertilisation|


Dans la couche plan de ferme, nous avons l'information suivante:

|  Colonne|  Description|
|--:|--:|
|  client|  Code du client|
|  ferme|  Nom de l'entreprise ou du groupe de champ|
|  champ|  Nom de la parcelle|
|  sup|  Superficie en hectare|
|  supepnd|  Superficie épandable en hectare|
|  serie|  Nom de la série de sol|
|  texture|  Groupe de texture de surface|
|  ville|  Nom de la municipalité|
|  mrc|  Nom de la MRC|
|  region|  Nom de la région|
|  lot|  Numéro de lot|
|  zmaisgr|  Zonage système collectif maïs-grain|
|  zcereeal|  Zonage système collectif céréales et maïs fourrager|
|  datemod|  Date de la dernière modification|
|  retpuit|  Superficie retirée en raison d'un puit|
|  retfoss|  Superficie retirée en raison d'un fossé|
|  reteau|  Superficie retirée en raison d'un cours d'eau|
|  rettot|  Superficie retirée totale|
|  locatio|  Est-ce que la parcelle est louée|
|  diagramme|  Nom de la page, utilisé pour les atlas|
|  angleatlas|  Angle de la page dans les atlas|
|  tri|  Colonne virtuelle servant à trier les champs adéquatement dans les mises en page|


### Sous-groupe Commun

|  Couche|  Description|
|--:|--:|
|  Base de données client|  Couche contenant l'information sur le client (nom, adresse, etc.)|
|  Maison|  Couche contenant les contour des maisons|
|  Lot cadastre rénové|  Couche contenant les limites des lots, mais ne contient pas les numéro de lot, doit être saisie manuellement|
|  Observation|  Couche contenant des observations ponctuelles faîtes au champ|
|  Puit|  Couche contenant l'emplacement des puits|
|  Fossé|  Couche contenant l'emplacement des fossés|
|  Amas|  Couche contenant l'emplacement des amas|

### Sous-groupe Parcelles agricoles


|  Couche|  Description|
|--:|--:|
|  Parcelles agricoles|  Couche contenant la Base de données des parcelles et productions agricoles déclarées de la FADQ ainsi que d'autres information|


### Sous-groupe Hydrologie


|  Couche|  Description|
|--:|--:|
|  Cours d'eau|  Couche contenant les entités linéaire de la Géobase du réseau hydrographique du Québec|
|  Cours d'eau SIGA|  Couche vide servant à ceux qui auraient leurs propre couche de cours d'eau|
|  Surface eau|  Couche contenant les entités polygones de la Géobase du réseau hydrographique du Québec|
|  Surface eau SIGA|  Couche vide servant à ceux qui auraient leurs propre couche de Surface eau|

### Sous-groupe Milieux Humides (WMS)

|  Couche|  Description|
|--:|--:|
|  Milieux humides potentiels|  Couche WMS des milieux humides potentiels|



### Sous-groupe Limites administratives (WMS)

|  Couche|  Description|
|--:|--:|
|  Routes|  Couche WMS des routes|
|  Adresse|  Couche WMS des Adresses|
|  Municipalité|  Couche WMS des municipalité|

### Sous-groupe Cadastre (WMS)

|  Couche|  Description|
|--:|--:|
|  Cadastre rénové|  Couche WMS du cadastre rénové|
|  Compilation cadastrale|  Couche WMS des lots avant la rénovation du cadastre|

### Sous-groupe Atlas

|  Couche|  Description|
|--:|--:|
|  Atlas|  Couche virtuelle servant dans la génération d'atlas|


### Sous-groupe Fond de carte (WMS)

|  Couche|  Description|
|--:|--:|
|  Orthophoto 2018|  Orthophoto du québec datant de 2018|
|  Carte de base du gouv. du Québec|  Carte de base tel que présente sur différentes carte du gouvernement du Québec|
|  Bing virtualearth|  Fond de carte satellite de Bing|
|  Google map, satellite, hybride|  Fond de carte satellite de Google|
|  Esri satellite|  Fond de carte satellite de ESRI|




## 5. Sélectionnez les parcelles du client et copiez-collez les dans plan de ferme


Pour ajouter des parcelles à notre plan de ferme du client, on clique sur parcelle agricole, puis on sélectionne les parcelles qu'on souhaite ajouter. On fait copier (ctrl+c), on clique sur le plan de ferme, on démarre le mode édition et on fait coller (ctrl+v). On peut soit faire une parcelle à la fois ou en sélectionner plusieurs d'un coup. Si la parcelle n'est pas dans la couche parcelle agricole, vous allez devoir la numériser dans le plan de ferme.


{{< figure library="true" src="gif/selection_parcelle.gif" title="Sélectionnez les parcelles du client et copiez-collez les dans plan de ferme" lightbox="true" >}}



Si vous avez un shapefile contenant les parcelles de votre client (FADQ, SIGA, etc.), vous devriez charger ce fichier dans QGIS. Une fois que vous vous êtes assuré que les parcelles sont au bon endroit, utilisez le script "importer plan de ferme". Ce script renommera les colonnes et tentera d'aller chercher l'information contenues dans la couche parcelle agricole. Une fois exécuté, vous pouvez copier-coller les entités de la couche "À enregistrer" vers la couche plan de ferme. 



## 6. Numérisez les contraintes (puits, fossé, cours d'eau)

Pour les puits et les fossés, il faut les numériser, donc on clique sur la couche appropriée, et on ajoute des entités. Pour les cours d'eau, la couche de cours d'eau de la Géobase du réseau hydrographique du Québec est déjà dans le projet, vous pourriez la modifier si vous le désirez.


{{< figure library="true" src="gif/numeriser_puits_fosse.gif" title="Numérisez les contraintes (puits, fossé, cours d'eau)" lightbox="true" >}}

## 7. Chargez le modèle zone_tampon


Pour charger un modèle, on doit ouvrir la boîte à outils. Dans la boîte à outil dans le haut, on clique sur l'icône modèle puis ajoutée un modèle. Dans le dossier commun/script du projet que vous avez téléchargé se trouvent différents modèles, on va aller chercher le modèle zone_tampon.


{{< figure library="true" src="gif/chargerscript.gif" title="Chargez le modèle zone_tampon" lightbox="true" >}}

chargerscript



## 8. Utilisez le modèle zone_tampon

Dans la boîte à outils sous modèle-plan de ferme, on double-clique sur zone_tampon. On choisit les couches appropriées et les distances requises. On clique sur exécuter.


{{< figure library="true" src="gif/zonetampon.gif" title="Utilisez le modèle zone_tampon" lightbox="true" >}}


## 9. Copiez-collez les entités et supprimez les entités précédentes

On sélectionne toutes les entités de la couche "À enregistrer" puis on les copie-colle dans la couche plan de ferme. On vient de dupliquer notre couche plan de ferme, nous allons ouvrir la table d'attributs, inverser la sélection puis supprimer les entités en double.


{{< figure library="true" src="gif/ajouteraplandeferme.gif" title="Copiez-collez les entités et supprimez les entités précédentes" lightbox="true" >}}




## 10. Renommez les champs et supprimez les couches temporaires

La couche parcelle agricole ne contient pas les numéros de parcelle, si l'on souhaite avoir les numéros de parcelle, nous devons allez saisir l'information dans la table d'attribut de plan de ferme.


{{< figure library="true" src="gif/renommer.gif" title="Renommez les champs et supprimez les couches temporaires" lightbox="true" >}}





## 11. Ouvrez la mise en page et prenez un des modèles de mise en page


Cliquez sur l'icône ...Dans le projet démo,nous avons mis 6 modèles. Sélectionnez un des modèles où ce n'est pas écrit "Atlas". 


{{< figure library="true" src="gif/miseenpage.gif" title=" Ouvrez la mise en page et prenez un des modèles de mise en page" lightbox="true" >}}




## 12. Replacez la carte

En cliquant sur la carte, dans les onglet à droite on voit Propriétés de l'objet. Dans cet onglet, nous avons un bouton pour replacer la carte selon ce que l'on voit sur QGIS.



{{< figure library="true" src="gif/replacercarte.gif" title=" Replacez la carte" lightbox="true" >}}


## 13. Modifiez l'information

Sur la carte, nous avont pré-défini différentes informations. Si vous souhaitez les modifier il suffit de cliquer avec l'outil de sélection sur l'objet en question et dans l'onglet paramèetre de l'objet modifier les options. Pour plus d'information sur la mise en page vous pouvez consulter cette page.


{{< figure library="true" src="gif/modifcarte.gif" title=" Replacez la carte" lightbox="true" >}}


## 14. Imprimez en PDF

Cliquez sur l'icône PDF pour enregistrer la carte ne format PDF.

{{< figure library="true" src="gif/enregistrerpdf.gif" title="Imprimez en PDF" lightbox="true" >}}

 
## 15. Enregistrez le projet

N'oubliez pas d'enregistrer le projet.

