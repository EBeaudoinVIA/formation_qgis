---
date: "2020-05-19"
diagram: true
image:
  caption: "Crédit photo: [**Elena Koycheva**](https://unsplash.com/photos/GUYCM0jhuSA)"
  placement: 3
math: true
title: 10 recommandations pour débuter avec QGIS
---


## 10 - Google

QGIS possède une immense communauté d'utilisateurs particulièrement actif sur internet. Si vous cherchez comment faire quelque chose, il est très fréquent de trouver un tutoriel montrant exactement comment faire. Il suffit de faire une recherche avec le mot "QGIS" sur un moteur de recherche pour trouver ce que l'on cherche. Malgré qu'il y est beaucoup de contenu en français, il est souvent plus facile de faire les recherches en anglais.


## 9 - Il y a souvent plusieurs façon de faire quelque chose, essayez en plusieurs et prenez la plus efficace

Il n'y a généralement pas une seule façon d'arriver au résultat que vous souhaitez. Essayer de déconstruire le problème, évaluer quelle sont les étapes pour y arriver. Des fois les étapes doivent être faites en ordre, des fois non. En règle générale, prioriser les étapes qui réduise la quantité d'information, elles vont accélérer les autres étapes (par example sélectionner les parcelles avant de faire un tampon).


## 8 - Enregistrez souvent
 
Il est facile de faire des erreurs dans QGIS, enregistrez votre projet souvent, et évitez les couches en mémoire temporaire sauf si vous savez ce que vous faites. QGIS bogue assez souvent, c'est désagréable de tout perdre. 

 
## 7 - Ayez de l'équipement performant

Il n'y a pas vraiment de minimum au niveau de l'équipement pour faire fonctionner QGIS, mais si possible essayez de l'utiliser sur vos meilleurs ordinateurs à disposition. L'élément le plus limitant en géomatique est généralement la mémoire vive (RAM), visez au minimum 6go. Si vous pouvez avoir deux écrans et une souris avec molette de défilement, c'Est vraiment utile.


## 6 - Soyez prudent avec les extensions

En date du 19 mai 2020, il y avait 667 extensions disponibles dans QGIS. Certaines de ces extensions sont très spécifiques alors que d'autres ajoute des fonctionnalité très utiles pour un grand nombre d'utilisateurs. Certaines fonctionne très bien, d'autres vont causer des bogues dans QGIS. Vérifier le nombre de téléchargement, c'est souvent un bon indicateur de la qualité de l'extension.




## 5 - Si quelque chose prend trop de temps ou pas assez de temps, il y a un problème

Soyez attentif au temps que prend vos algorithmes. Il peut arriver que vos algorithmes prennent pas assez ou trop de temps, c'est un signe qu'il y a eu une erreur. Par exemple si c'est trop long, vous avez peut-être pris une couche plus lourde, si c'Est trop court, vérifier la sortie de l'algorithme, il est possible que la couche soit vide.  



## 4 - Enregistrez souvent

## 3 - N'ayez pas peur de cliquer partout

Dans QGIS il y a des boutons, des menus et des options partout, certaines sont à plusieurs endroit d'autres à un seul endroit. Fouiller, cliquer sur les différents menus et boutons, essayer les algorithmes, vous allez trouver une façon de travailler qui vous convient. Mais n'oubliez pas d'enregistrer votre projet avant de faire ces test :-p.



## 2 - Gérez bien vos dossier


Il est facile de perdre le contrôle sur l'organisation des dossiers. D'arriver dans un dossier et d'avoir une dizaine de ocuche, ne plus savoir ce quelle contiennent et donc de se partir un nouveau sous-dossier ou on va recréer un grand nombre de couche. Planifiez votre gestion de dossier et quelle information stocker dans chaque couche, ce temps mis au départ va vous sauvez beaucoup de temps par la suite. Si vous travailler sur des projets de plus grande envergure avec plus de personne impliqué, pensez à rédiger des métadonnées pour bien expliquer votre organisation d'information.

N'oubliez pas de ne pas mettre de caractère spéciaux dans dans le nom des fichier ou des dossiers.

{{< figure library="true" src="img/misc/gaston_lagaffe.jpg" title="Ne mettez pas de caractères spéciaux! source: Gaston Lagaffe" lightbox="true" >}}


## 1 - Vérifiez les projections de vos couches et du projet

C'est l'erreur la plus fréquente, si vos couches n'ont pas la même projection, vous ne pourrez pas utiliser d'algorithme sur ces couches. 