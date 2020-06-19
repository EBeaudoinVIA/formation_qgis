---
date: "2020-06-19"
diagram: true
image:
  caption: "Crédit photo: [**Annie Spratt**](https://unsplash.com/photos/AFB6S2kibuk)"
  placement: 3
math: true
numbersections: true
title: Faire un plan de ferme en 20 étapes
---

Voici la procédure simple pour faire un plan de ferme pour un nouveau client et de calculer la superficie épandable.

## 1. Téléchargez le projet démo

Pour facilitr votre travail dans QGIS, nous avons préparé des projets préconfigurés, contenant les couches d'informations requises, des styles et des mises en page prédéfinies. Nous vous invitons à télécharger un des modèles divisé par région administrative ci-dessous. 


<iframe src="https://drive.google.com/embeddedfolderview?id=1XXKXesdTfglVrqOAHMuY6uvCyp07pcso#list" width="100%" height="500" frameborder="0"title=”Projet démo par région administrative"></iframe>

## 2. Dézippez le projet démo

Avant de travailler avec le projet, il faut le dézipper. Cliquer droit sur le fichier téléchargé puis faites extraire tout.

## 3. Dupliquez le client démo

Une fois dézippé, on clique sur le dossier "client_demo", puis on fait copier-coller pour le dupliquer. On le renomme avec le nom de notre client.


## 4. Ouvrez le projet
 
Dans le dossier nouvellement créer, on renomme le projet "client_demo.qgz" pour le nom de notre client. Ensuite on double-clique dessus pour l'ouvrir. 

## 5. Description de l'information dans le projet

Dans le projet qu'on vient d'ouvrir, nous avons déjà ajouté plusieurs couches. Voici la liste des couches et une brève description.


## 6. Sélectionnez les parcelles du client


Pour ajouter des parcelles à notre plan de ferme du client, on clique sur parcelle agricole, puis on sélectionne les parcelles qu'on souhaite ajouter. 



## 7. Copiez-collez dans la couche plan de ferme

On fait copier (ctrl+c), on clique sur le plan de ferme, on démarre le mode édition et on fait coller (ctrl+v). On peut soit faire une parcelle à la fois ou en sélectionner plusieurs d'un coup. Si la parcelle n'est pas dans la couche parcelle agricole, vous allez devoir la numériser dans le plan de ferme.



## 8. Numérisez les contraintes (puits, fossé, cours d'eau)

Pour les puits et les fossés, il faut les numériser, donc on clique sur la couche approprié, et on ajoute des entités. Pour les cours d'eau, la couche de cours d'eau de ... est déjà dans le projet, vous pourriez la modifié si vous le désirez.

  
## 9. Chargez le modèle "zone_tampon"


Pour charger un modèle, on doit ouvrir la boîte à outil. Dans la boîte à outil dans le haut, on clique sur l'icone modèle puis ajouter un modèle. Dans le dossier commun/script du projet que vous avez téléchargé, se trouve différents modèle, on va aller chercher le modèle zone_tampon.


## 10. Utilisez le modèle "zone_tampon"

Dans la boite à outil sous modèle-plan de ferme, on double-clique sur zone_tampon. On choisi les couches appropriés et les distance requises. On clique sur exécuter.


## 11. Copiez-collez les entités

On sélectionne toute les entités de la couche "À Enregistrer" puis on les copie-colle dans la couche plan de ferme.


## 12. Supprimez les entités précédentes


On vient de dupliquer notre couche plan de ferme, nous allons ouvrir la table d'attributs, inverser la sélection puis supprimer les entités en double.

## 13. Renommez les champs

La couche parcelle agricole ne contient pas les numéro de parcelle, si l'on souhaite avoir les numéro de parcelle, nous devons allez saisir l'information dans la table d'attribut de plan de ferme.


## 14. Enregistrez la couche et supprimez les couches temporaires




## 15. Ouvrez la mise en page


Cliquez sur l'icône ...


## 16. Prenez un des modèles de mise en page

Dans le projet démo,nous avons mis 6 modèles. Sélectionnez un des modèles où ce n'est pas écrit "Atlas". 



## 17. Replacez la carte

En cliquant sur la carte, dans les onglet à droite on voit Propriétés de l'objet. Dans cet onglet, nous avons un bouton pour replacer la carte selon ce que l'on voit sur QGIS.



## 18. Modifiez l'information

Sur la carte, nous avont pré défini différentes informations. Si vous souhaitez les modifier il suffit de cliquer avec l'outil de sélection sur l'objet en question et dans l'onglet paramèetre de l'objet modifier les options. Pour plus d'information sur la mise en page vous pouvez consulter cette page.





## 19. Imprimez en PDF

Cliquer sur l'icône PDF pour enregistrer la carte ne format PDF.

 
## 20. Enregistrez le projet

N'oublier pas d'enregistrer le projet.
