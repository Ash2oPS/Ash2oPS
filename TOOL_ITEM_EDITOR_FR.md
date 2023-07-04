<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>

---



<div align="center">

# :banana: Éditeur d'Items :coconut:

<img src="Resources/Images/I_ItemEditor_Banana_01.png" alt=Banana width="35%" height="80%">
<br>
<br>
</div>

- [Qu'est-ce donc ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ITEM_EDITOR_FR.md#quest-ce-donc-)
- [Quelques exemples d'objets](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ITEM_EDITOR_FR.md#quelques-exemples-dobjets)
- [Item Functions](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_ITEM_EDITOR_FR.md#item-functions)


## Qu'est-ce donc ?


Just Leave Already! est le projet étudiant de mon groupe créé pour la fin d'année scolaire 2022-2023. Vous pouvez le 
retrouver sur itch.io [ICI](https://ash2o.itch.io/just-leave-already). Dans JLA!, vous incarnez Bob, un 
homme ayant élu domicile sur une île déserte. Voyant cette dernière se faire envahir par des touristes ne
respectant rien sur leur passage, Bob décide de les faire fuire de toutes les façons possibles.
<br>
Dans ce bac à sable, vous devez utiliser les objets mis à votre disposition pour détruire les constructions des
envahisseurs. En tant que développeurs, nous avons donc eu besoin de créer ces objets. La façon la plus 
efficace de s'y prendre était de créer un éditeur d'objets de façon à ce que chaque membre du groupe puisse 
créer les objets qu'il désire sans avoir à écrire la moindre ligne de code.

## Quelques exemples d'objets



<div align="center">

<img src="Resources/Images/I_ItemEditor_Dynamite_01.png" alt=Dynamite width="28%" height="80%">
<img src="Resources/Images/I_ItemEditor_Banana_01.png" alt=Banana width="28%" height="80%">
<img src="Resources/Images/I_ItemEditor_Blower_01.png" alt=Blower width="28%" height="80%">

</div>
<br>

Par exemple, ces trois objets, à savoir, une dynamite, une banane et une souffleuse, sont des objets créés via
cet éditeur. Si nous regardons de plus près la dynamite, voici à quoi cela ressemble :

<br>

<div align="center">

<img src="Resources/Images/I_ItemEditor_Dynamite_02.png" alt=Dynamite width="60%" height="80%">
<br>
<img src="Resources/Images/I_ItemEditor_Dynamite_03.png" alt=Dynamite width="60%" height="80%">

</div>
<br>


Comme vous pouvez le voir, chaque caractéristique de l'objet peut-être modifiée ici, commençant par son mesh,
jusqu'à ses fonctions appelées lors de son utilisation. L'utilisateur peut déterminer si un objet peut être 
porté, jeté ou utilisé. S'il peut être jeté par exemple, vous pouvez déterminer la puissance avec laquelle il 
est lancé. De la même façon vous pouvez vraiment modifier toutes les caractéristiques souhaitée par la 
personne. Des sécurités ont été mises en place pour éviter les possibles erreurs causées par l'utilisateur. 
De ce fait, rendre l'objet lançable mais non attrapable fait apparaître un message d'erreur, puisqu'un objet 
ne peut être lancé si le joueur est dans l'incapacité de l'attraper.

<br>
<div align="center">

<img src="Resources/Images/I_ItemEditor_SafetyMessage_01.png" alt=Dynamite width="60%" height="80%">

</div>
<br>


## Item Functions

<div align="center">

`[Section en cours de création]`

</div>


Afin de rendre un objet unique, le plus important reste de lui conférer une ou plusieurs utilités qui vont 
pousser le joueur à préférer tel objet dans telles circonstances plutôt qu'un autre. C'est alors qu'entrent
en jeu les **`Item Functions`**. 
<br>
Les Item Functions sont des classes descendant de ScriptableObject, et chacune d'entre elles possède une 
fonction principale appelée par l'Item. Au moment de créer l'objet via l'éditeur, ce dernier vient créer des 
instances des item functions sélectionnées, et vient les attacher à l'asset en tant que sub-object.

<br>
<div align="center">

<img src="Resources/Images/I_ItemEditor_ItemFunction_01.png" alt=ItemFunction1 width="60%" height="80%">
<br>
<img src="Resources/Images/I_ItemEditor_ItemFunction_02.png" alt=ItemFunction2 width="75%" height="80%">
<br>

*Exemple d'objet pouvant faire spawner un objet, souffler, exploser et faire spawner un GameObject.*

</div>
<br>

Une fois ces fonctions codées, il ne reste plus qu'à les sélectionner dans l'item en cours de création. 
Elles seront alors appelée au moment souhaité.


Avec l'ensemble de ces features présentes dans cet éditeur, je suis heureux de pouvoir dire qu'il a apporté 
une aide considérable dans la production de notre jeu de fin d'études. Les objets étant au coeur du 
gameplay, n'importe quel membre de mon équipe a pu créer ce qu'il souhaitait facilement et rapidement, et ce,
sans avoir besoin de coder quoi que ce soit.


---

<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>
