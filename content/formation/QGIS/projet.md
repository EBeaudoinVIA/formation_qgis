---
date: "2019-05-05T00:00:00+01:00"
draft: false
linktitle: Projet
menu:
  example:
    parent: QGIS
    weight: 2
title: Projet
toc: true
type: docs
weight: 2
---

The state of your QGIS session is called a project. QGIS works on one project at a time. A settings can be project-specific or an application-wide default for new projects (see section Options). QGIS can save the state of your workspace into a QGIS project file using the menu options Project ‣ fileSave Save or Project ‣ fileSaveAs Save As….

Lorsque vous travaillez dans QGIS, vous travaillez dans un **Projet**. Ce projet ne contient pas vos couches d'information, mais des liens vers vos données. Si vous déplacez le projet et/ou les données, vous risquez de ne plus pouvoir utiliser votre projet ou du moins devoir refaire les liens. 


Un projet contient entre autres:

* Un lien vers les couches de données

* Le style des couches

* La localisation du canevas

* Les mises en pages

Il est utile d'avoir un projet par client ou par dossier. Vous pouvez y revenir plus tard et faire juste une modification rapide.

Les projets QGIS sont enregistrés avec l'extension .qgz. Il s'agit en fait d'un fichier .zip contenant un fichier.qgs. Ce fichier est en fait un document XML donc éditable dans un éditeur de texte. Si vous modifiez les projets ainsi, faites-vous une bonne sauvegarde de sécurité puisque c'est facile de faire une erreur.

Le format des fichiers de projet change fréquemment, il est possible qu'un projet fait avec une version de QGIS ne fonctionne plus avec des versions ultérieures du logiciel.

