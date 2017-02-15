
#Comment modifier le site
<br><br>

le site vient du template [feeling responise](https://phlow.github.io/feeling-responsive/design/grid/).
On devrait pouvoir faire ce que tu peux voir la. 

Pour l'instant, si on se limite au pages qui sont deja crees. 
<br><br><br>

## La page d'acceuil 
pas en acces facile pour l'instant.
<br><br><br>

## Pour editer les differentes autres pages

Editer uniquement les fichiers qui sont dans le repertoire "page/" et qui ont une extension .md

chaque fichier corresponds a une page du site

1. music.md
2. video.md
3. photo.md
4. info.md

**Important:**
Dans chaque fichier ne pas toucher aux lignes en haut entre les deux "---"
aussi ne pas supprimer la ligne `<p></p>` a la fin de chaque fichier

le format pour ecrire s'appelle markdown tu peux trouver des exemples [ici](https://fr.wikipedia.org/wiki/Markdown)

Pour l'instant ne touche pas au reste des fichiers & repertoires dans "page/"
- redirected_page.md
- pages-root-folder/
- original/
<br><br><br>

Pour les pages Musique, Video et Photo j ai ajoute dessous quelques infos.

#### Musique
Pour ajouter un morceau de musique avec un player, inclure dans le fichier la ligne suivante.

    <audio src="http://blabla.com/monblabla.mp3" type="audio/mp3" controls="controls"></audio>

avec l'adresse de ou est le fichier mp3, ici `http://blabla.com/monblabla.mp3`
<br><br><br>


#### Video
Pour ajouter une video youtube, inclure dans le fichier les lignes suivantes.

    <div class="flex-video">
        <iframe width="420" height="315" src="//www.youtube.com/embed/_SM6nuYigaw" frameborder="0" allowfullscreen></iframe>
    </div>

avec le lien "embed" de youtube qui est ici `_SM6nuYigaw` pour la video de patroupal.
Clique [ici][4] pour regarder comment recuperer le lien dans le tutoriel Youtube.
<br><br><br>


#### Photo

**pour inclure une photo:**
ajouter la photo dans repertoire "images/" du repositery github, 
puis include dans le fichier .md la ligne suivante. 

    <img class="t60" src="{{ site.urlimg }}header_homepage_13.jpg" alt="">

ou `header_homepage_13.jpg` est le nom du fichier. ne pas modifier le reste. l'image sera de la larger de la zone de texte.


**pour inclure une gallerie de photo**
dans ce cas il faut modifier la partie haute (entre les 2 "---") du fichier .md pour y definir les images de la gallerie.
par exemple pour les images de la repete de janvier 2017 ajouter:

    repete2017:
		- image_url: 2017-repete/DSC4351_modified.jpeg
		  #caption: Great images by Ronny
		- image_url: 2017-repete/DSC4424_modified.jpeg
		  #caption: Great images by Ronny

Les fichier photos doivent etre dans le repertoire "images/" du repositery github. Chaque image doit etre accompagnee d'une copie de taille reduite (ici `226px × 150px`) qui sert pour la gallerie. Pour une image nommee `XXX.jpeg` le nom de l'image reduite doit etre `XXX-thumb.jpeg`. 
Dans l'exemple de la gallerie de la repete de janvier 2017, toutes les images sont dans le repertoire "images/2017-repete/".

Ensuite il suffit d'ajouter dans le fichier .md la ou on veut metter la gallerie:

    {% include gallery gallery_name="repete2017" %}
    

<br><br><br>





[4]: https://www.youtube.com/watch?v=lJIrF4YjHfQ
