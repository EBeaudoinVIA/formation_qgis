---
date: "2020-05-19"
diagram: true
image:
  caption: "Crédit photo: [**Elena Koycheva**](https://unsplash.com/photos/GUYCM0jhuSA)"
  placement: 3
math: true
title: 10 recommandations pour débuter avec QGIS
---

Voici 10 recommandations (vous pouvez les voir comme des commandements!) afin de faciliter votre transition vers QGIS.


## 10 - Google

QGIS possède une immense communauté d'utilisateurs. Si vous cherchez comment faire quelque chose, il est très fréquent de trouver un tutoriel montrant exactement comment faire. Il suffit de faire une recherche avec le mot "QGIS" dans un moteur de recherche pour trouver ce que l'on cherche. Malgré qu'il y ait beaucoup de contenu en français, il est souvent plus facile de faire les recherches en anglais.


## 9 - Il y a souvent plusieurs façons de faire quelque chose, essayez-en plusieurs et prenez la plus efficace

Il n'y a généralement pas qu'une seule façon d'arriver au résultat que vous souhaitez. Essayez de déconstruire le problème, évaluez quelles sont les étapes pour y arriver. Des fois les étapes doivent être faites en ordre, des fois non. En règle générale, prioriser les étapes qui réduise la quantité d'information, elles vont accélérer les autres étapes (par exemple sélectionner les parcelles avant de faire un tampon).


## 8 - Enregistrez souvent
 
Il est facile de faire des erreurs dans QGIS, enregistrez votre projet souvent, et évitez les couches en mémoire temporaire sauf si vous savez ce que vous faites. QGIS bogue assez souvent, c'est désagréable de tout perdre. 

 
## 7 - Ayez de l'équipement performant

Il n'y a pas vraiment de minimum au niveau de l'équipement pour faire fonctionner QGIS, mais si possible essayer de l'utiliser sur vos meilleurs ordinateurs à disposition. L'élément le plus limitant en géomatique est généralement la mémoire vive (RAM), visez au minimum 6 go. Si vous pouvez avoir deux écrans et une souris avec molette de défilement, c'est vraiment utile.


## 6 - Soyez prudent avec les extensions

En date du 19 mai 2020, il y avait 667 extensions disponibles dans QGIS. Certaines de ces extensions sont très spécifiques alors que d'autres ajoutent des fonctionnalités très utiles pour un grand nombre d'utilisateurs. Certaines fonctionnent très bien, d'autres vont causer des bogues dans QGIS. Vérifier le nombre de téléchargements, c'est souvent un bon indicateur de la qualité de l'extension.




## 5 - Si quelque chose prend trop de temps ou pas assez de temps, il y a un problème

Soyez attentif au temps que prennent vos algorithmes. Il peut arriver que vos algorithmes ne prennent pas assez ou trop de temps, c'est un signe qu'il y a eu une erreur. Par exemple si c'est trop long, vous avez peut-être pris une couche plus lourde, si c'est trop court: vérifiez la sortie de l'algorithme, il est possible que la couche soit vide.  



## 4 - Enregistrez souvent

Ça fait longtemps que vous n'avez pas enregistré!

## 3 - N'ayez pas peur de cliquer partout

Dans QGIS il y a des boutons, des menus et des options partout, certaines sont à plusieurs endroits d'autres à un seul endroit. Fouillez, cliquez sur les différents menus et boutons, essayez les algorithmes, vous allez trouver une façon de travailler qui vous convient. Mais n'oubliez pas d'enregistrer votre projet avant de faire ces tests.



## 2 - Gérez bien vos dossiers


Il est facile de perdre le contrôle sur l'organisation des dossiers, d'arriver dans un dossier et d'avoir une dizaine de couches, ne plus savoir ce quelle contiennent et donc de se partir un nouveau sous-dossier. Planifiez votre gestion de dossier et quelle information stocker dans chaque couche, ce temps mis au départ va vous sauvez beaucoup de temps par la suite. Si vous travaillez sur des projets de plus grande envergure avec plus de personnes impliquées, pensez à rédiger des métadonnées pour bien expliquer votre organisation d'information.

N'oubliez pas de ne pas mettre de caractère spécial dans le nom des fichiers ou des dossiers.

{{< figure library="true" src="img/misc/gaston_lagaffe.jpg" title="Ne mettez pas de caractères spéciaux!" lightbox="false" >}}


## 1 - Vérifiez les projections de vos couches et du projet

C'est l'erreur la plus fréquente, si vos couches n'ont pas la même projection, vous ne pourrez pas utiliser d'algorithme sur ces couches. 
