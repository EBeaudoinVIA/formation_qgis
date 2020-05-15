---
date: "2019-07-12"
diagram: true
image:
  caption: "Crédit photo: [**Rock'n Roll Monkey**](https://unsplash.com/photos/R4WCbazrD1g)"
  placement: 3
math: true
title: Utiliser des modeles dans QGIS
---


Il est possible d'automatiser des tâches dans QGIS. Cet article va montrer comment utiliser la méthode la plus simple (le modeleur graphique) pour obtenir l'attribut occupant la plus grande proportion d'une intersection. 

Si je souhaite obtenir dans quelle ville se trouve un champ, et que je ne suis pas intéressé à savoir si elle se trouve dans plus d'une ville, je dois faire une série de plusieurs opérations dans QGIS. Sans être très longue à réaliser, cette accumulation d'opération peut être désagréable, surtout si on oublie une étape. Pour accélérer le processus, on peut créer un **modèle**.

La première étape est de démarrer le modeleur graphique.

![](/img/img/bouton/processingModel.png)

{{< figure library="true" src="gif/start_modeler.gif" title="Ouvrir le modeleur" lightbox="true" >}}


Ensuite on dénifit les entrées du modèle

{{< figure library="true" src="gif/model_input.gif" title="Entrée du modèle" lightbox="true" >}}

On calcul ensuite l'intersection entre les couches

{{< figure library="true" src="gif/model_intersect.gif" title="Intersection" lightbox="true" >}}

À tous moments, on peut vérifier le fonctionnement du modèle en nommant une sortie

{{< figure library="true" src="gif/model_test.gif" title="Tester le modèle" lightbox="true" >}}

On trie ensuite les polygones d'intersection par superficie

{{< figure library="true" src="gif/model_tri.gif" title="Trier par superficie" lightbox="true" >}}

On fait une jointure par localisation pour terminer

{{< figure library="true" src="gif/model_joint.gif" title="Jointure par localisation" lightbox="true" >}}

On test pour être sur d'avoir le résultat qu'on souhaite

{{< figure library="true" src="gif/model_testfin.gif" title="Test final" lightbox="true" >}}

On enregistre le modèle

{{< figure library="true" src="gif/model_save.gif" title="Enregistrer le modèle" lightbox="true" >}}

Le modèle est maintenant disponible dans la boîte à outils

{{< figure library="true" src="gif/model_toolbox.gif" title="Le modèle est dans la boîte à outils" lightbox="true" >}}

Vous pouvez maintenant partager votre modèle avec vos collègues. Il suffit de leur envoyer le fichier .model3 que vous venez de créer. Vos collègues doivent ensuite allez le placer dans le dossier des modèles QGIS (par défaut sur windows `%appdata%\QGIS\QGIS3\profiles\default\processing\models` )



