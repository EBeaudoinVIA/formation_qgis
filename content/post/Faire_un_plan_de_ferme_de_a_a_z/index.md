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




## 4. Description du projet

Dans le projet qu'on vient d'ouvrir, nous avons déjà ajouté plusieurs couches. Voici la liste des couches ainsi qu'une brève description.





## 5. Sélectionnez les parcelles du client et copiez-collez les dans plan de ferme


Pour ajouter des parcelles à notre plan de ferme du client, on clique sur parcelle agricole, puis on sélectionne les parcelles qu'on souhaite ajouter. On fait copier (ctrl+c), on clique sur le plan de ferme, on démarre le mode édition et on fait coller (ctrl+v). On peut soit faire une parcelle à la fois ou en sélectionner plusieurs d'un coup. Si la parcelle n'est pas dans la couche parcelle agricole, vous allez devoir la numériser dans le plan de ferme.


{{< figure library="true" src="gif/selection_parcelle.gif" title="Sélectionnez les parcelles du client et copiez-collez les dans plan de ferme" lightbox="true" >}}





## 6. Numérisez les contraintes (puits, fossé, cours d'eau)

Pour les puits et les fossés, il faut les numériser, donc on clique sur la couche appropriée, et on ajoute des entités. Pour les cours d'eau, la couche de cours d'eau de ... est déjà dans le projet, vous pourriez la modifié si vous le désirez.


{{< figure library="true" src="gif/numeriser_puits_fosse.gif" title="Numérisez les contraintes (puits, fossé, cours d'eau)" lightbox="true" >}}

## 7. Chargez le modèle "zone_tampon"


Pour charger un modèle, on doit ouvrir la boîte à outils. Dans la boîte à outil dans le haut, on clique sur l'icône modèle puis ajoutée un modèle. Dans le dossier commun/script du projet que vous avez téléchargé se trouvent différents modèles, on va aller chercher le modèle zone_tampon.


{{< figure library="true" src="gif/chargerscript.gif" title="Chargez le modèle "zone_tampon"" lightbox="true" >}}

chargerscript



## 8. Utilisez le modèle "zone_tampon"

Dans la boîte à outils sous modèle-plan de ferme, on double-clique sur zone_tampon. On choisit les couches appropriées et les distances requises. On clique sur exécuter.


{{< figure library="true" src="gif/zonetampon.gif" title="Utilisez le modèle "zone_tampon"" lightbox="true" >}}


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
