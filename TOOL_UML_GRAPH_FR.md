<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>

---
<div align="center">

# :clipboard: UML Diagram Generator 📃


<br>
</div>

- [Qu'est-ce donc ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_UML_GRAPH_FR.md#quest-ce-donc-)
- [Quelle est l'idée derrière tout ça ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_UML_GRAPH_FR.md#quelle-est-lid%C3%A9e-derri%C3%A8re-tout-%C3%A7a-)
- [Qu'est fonctionnel à l'heure qu'il est ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_UML_GRAPH_FR.md#quest-fonctionnel-%C3%A0-lheure-quil-est-)
- [Et pour la suite ?](https://github.com/Ash2oPS/Ash2oPS/blob/main/TOOL_UML_GRAPH_FR.md#et-pour-la-suite-)

## Qu'est-ce donc ?

Le développement de cet outil a commencé il y a presque un an et a été annulé par manque de temps. Il devait servir au sein d'un projet
étudiant. Comme mes méthodes de travail ont bien évolué depuis, je prévois de potentiellement le recommencer de zéro puisqu'il 
s'agit d'un projet qui me tient à coeur.

<div align="center">
<img src="Resources/Images/I_UMLDiagram_01.png" alt= Blender width="80%" height="80%">

Exemple d'un Diagramme UML simple  
(source: https://medium.com/@uferesamuel/uml-class-diagrams-the-simple-approach-eee2d1ffc125)
</div>

Lorsqu'un projet prend de l'ampleur, garder son architecture en tête devient une tâche complexe qui reste bien 
importante. La solution un peu brutale serait de maintenir manuellement une documentation claire à jour régulièrement. 
Documentation qui énumèrerait tous les scripts du projet, les relations qu'ils partagent entre eux, leurs attributs, 
leurs méthodes, etc. Bien qu'efficace cette méthode est bien chronophage et est sujette à l'erreur humaine. Un 
générateur de diagramme UML serait bien pratique !

## Quelle est l'idée derrière tout ça ?

Le programme scanne de manière récursive un répertoire (de préférence le dossier `Script` d'un projet Unity) et récupère certaines 
informations pour chaque fichier `.cs` :

- Le nom de classe
- La classe dont elle dérive
- Ses attributs et ses méthodes
- Le `summary` de ces éléments

Avec ces informations, le programme est capable de générer un espace de travail dans lequel se tient une version simplifiée d'un 
diagramme UML pour chaque classe trouvée. Des flèchent indiquent le parenting de ces classes. Le graph d'une class affiche son nom, 
ses attributs, ainsi que ses méthodes. En survollant ces éléments avec la souris, un pop-up apparait possédant en tooltip le summary
de cet élément s'il en a un. À partir de là vous pouvez naviguer au sein de cet espace de travail ou bien exporter une copie sous forme
d'image du diagramme entier ou bien de seulement la partie qui vous intéresse.


<div align="center">
<img src="Resources/Images/I_UMLDiagramGenerator_01.png" alt= IsoMapGenDemo1 width="80%" height="80%">
</div>

## Qu'est fonctionnel à l'heure qu'il est ?

<div align="center">

`[Section en cours de création]`

</div>

## Et pour la suite ?

<div align="center">

`[Section en cours de création]`

</div>

---

<font size = "3"> 

[⬅️ Retour au Profil](https://github.com/Ash2oPS)

</font>
