<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>

---
<div align="center">

# :world_map: Isometric 2D Map Generator :triangular_ruler:

<img src="Resources/Images/I_IsoMapLogo.png" alt= Blender width="20%" height="30%">
<br>
</div>

- [Qu'est-ce donc ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ISOMETRIC_MAP_GENERATOR.md#what-is-it)
- [Paramètres de bloc](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ISOMETRIC_MAP_GENERATOR.md#block-parameters)
- [Map Skin](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ISOMETRIC_MAP_GENERATOR.md#map-skin)
- [Et pour la suite ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ISOMETRIC_MAP_GENERATOR.md#whats-next)



## Qu'est-ce donc ?

Bien souvent, créer une map pour un jeu 2D au style isométrique peut être chronophage et assez peu ergonomique selon les éditeurs. Une
fois tous les sprites de bloc crées, vous ouvrez votre programme de création de map, vous sélectionnez un bloc, vous dessinez la forme
que vous souhaitez, bloc après bloc, vous sélectionnez un autre bloc, vous dessinez la nouvelle forme souhaitée, mais finalement la zone
dessinée avec le premier bloc ne convient pas... Bref, vous avez compris, ce sont des opérations répétitives qui peuvent être longues
et potentiellement pénibles. Et c'est là qu'entre en jeu mon éditeur !  
Voici comment ça marche :

<br>
<div align="center">
<img src="Resources/GIFs/GIF_IsoMapGenerator_Demo_01.gif" alt= IsoMapGenDemo1 width="70%" height="70%">
</div>
<br>

Comme vous pouvez le voir, il permet de créer une map rapidement et facilement. Il prend simplement en input une texture low-res, en 
extrait les pixels de couleur ainsi que leurs coordonées. Avec ces informations et certains paramètres, il va pouvoir générer la map 
correspondante. Le style actuel des blocs est en pixel art, mais il peut être changé pour un style plus traditionnel ou autre, puisque
les sprites sont modifiables à la guise de l'utilisateur et une texture en input peut prendre en considération plusieurs couleurs pour
plusieurs types de blocs.


<br>
<div align="center">
<img src="Resources/GIFs/GIF_IsoMapGenerator_Demo_02.gif" alt= IsoMapGenDemo1 width="70%" height="70%">
</div>
<br>

## Paramètres de bloc

Chaque couleur de pixel correspond à un type de bloc que vous avez préalablement renseigné. Pour chaque bloc, en plus de pouvoir 
choisir son sprite, vous pouvez lui choisir des variations de couleurs, des mouvements de vague plus ou moins prononcés, des hauteurs
différentes, le tout dans l'optique de donner à chaque type de bloc son look unique. L'eau ou la lave par exemple ont une animation
de vague pour simuler leur nature liquide. La sable, lui, a une hauteur plus aléatoire pour lui donner son côté plus "chaotique".

<br>
<div align="center">
<img src="Resources/GIFs/GIF_IsoMapGenerator_Demo_03.gif" alt= IsoMapGenDemo1 width="70%" height="70%">
</div>
<br>

Pour utiliser pleinement les capacités de cet outils, il est conseillé de respecter une préparation spécifique des sprites. Au moment 
de les produire, il faut bien garder en tête que pour créer un type de bloc, il faut en réalité 2 sprites. Cela peut sembler contre-
productif, mais en réalité avec ce setup, il sera possible de résalier un très grand nombre de variations de blocs très rapidement. 
Nous avons donc besoin d'un sprite en échelle de gris qui représente les zones d'ombres et de lumières du bloc, ainsi qu'un sprite 
uniquement composé des couleurs rouge (#FF0000), verte (#00FF00) et bleue (#0000FF). Ce sprite aux allures un peu étranges va permettre
de déterminer la couleur appliquée au bloc au moment de sa création. Cette combinaison de sprites est alors traitée par un custom shader
afin de pouvoir créer énormément de variations.

<br>
<div align="center">
<img src="Resources/Images/I_IsoMapGenerator_SpriteBlock_01.png" alt= SpriteBlock01 width="50%" height="50%">
<img src="Resources/Images/I_IsoMapGenerator_SpriteBlock_02.png" alt= SpriteBlock02 width="85%" height="85%">
</div>
<br>

## Map Skin

Afin de regrouper et contrôler tous ces paramètres de blocs, la map possède un certain nombre de règles, le tout appelé le Map Skin.
Il est possible de créer autant de Map Skins que désiré et chacun d'entre eux détermine  

Pour contrôler tous ces paramètres de blocs, la carte est régie par un ensemble de règles appelé "Map Skin". Grâce à une "Map Skin",
vous pouvez définir la teinte globale des ombres, le sprite de bloc correspondant à une couleur de pixel spécifique de la texture, 
ainsi que les couleurs possibles pour ses composantes rouge, verte et bleue. J'ai bien dit "possibles" car si vous souhaitez que ce 
bloc présente des nuances légèrement différentes de celles de ses voisins, c'est tout à fait réalisable. En effet, au lieu d'utiliser 
des couleurs unies, vous pouvez utiliser des dégradés afin qu'une couleur soit choisie aléatoirement à l'intérieur de ce dégradé.


## Et pour la suite ?

Le développement de cet outil est actuellement en pause et nécessiterait quelques ajustements concernant son fonctionnement. 
Prenons un instant pour réfléchir à ce que nous pourrions en faire. Si nous le combinions avec un générateur de carte aléatoire, 
nous pourrions facilement créer des cartes aléatoires dans le style isométrique. Nous pouvons imaginer une révisite des Pokémon
Donjon Mystère dans ce style-là pourquoi pas.  
Si l'occasion et la nécessité se présentaient, cet outil pourrait être adapté pour être utilisé avec des meshes dans un environnement
3D.

---

<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>
