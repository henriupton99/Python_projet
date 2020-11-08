# Projet Python pour le Data Scientist

## Introduction

<p style="text-align:justify;">
Ce dépôt GitHub regroupe des éléments de recherche gravitant autour de la problématique suivante :
<center>### ***" Prédiction de la note d'un film à partir de ses principales caractéristiques "***</center>

L'objectif fut de construire un modèle de Machine Learning visant à prédire la note moyenne (spectateurs) qu'obtiendrait un film selon ses principales caractéristiques : genres principaux, durée, année de sortie, réalisateur, casting...


- *Sur quelles données les analyses ont-t-elles été menées ?*

Sur la base de données de l'IMDB (Interantional Movie Data Base). Grâce au très large panel de données recensées sur ce site, nous avons collecté des informations sur près de 450 000 films. Plus précisément, nous avons retenu leur **titre**, **année de sortie**, **durée**, **réalisateur** et **acteurs**, **genres principaux**. De plus nous avons pu récolter la **note moyenne des spectateurs** attribuée à chaque film, ainsi que le **nombre de votes** qui ont permis de la constituer.


- *Comment les données ont-elles été récoltées ?*
 
 La base de données assujettie à nos analyses et prédictions fut construite via des procédés de web scraping et crawling à partir du site de l'IMDB :
 https://www.imdb.com

 Une fois sur la page d'accueil, il est possible d'effectuer une recherche personnalisée de films, comme sur l'image qui suit : 

<p align="center">
  <img src= "images/image_1.png" width = "800"/>
</p>


Nos seuls critères furent d'exclure les autres catégories hors "films" à proporement parler (séries, émissions tv,..) et d'inclure les films comportant une limite d'âge. Nous obtenons ainsi une liste de près de 450 000 films. Cette liste est fractionnée en plusieures pages (250 films par page soit N = 450 000/250 = 1800 pages environ). Voici l'une de ces pages :

<p align="center">
  <img src="images/image_2.png" width = "800"/>
</p>


Il est facilement observable que toutes les informations convoitées sont visibles sur la page. Il ne restait donc plus qu'à web scraper ces éléments, puis répéter la collecte sur toutes les pages qui constituent la liste (crawling).

</p>