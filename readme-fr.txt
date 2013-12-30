  JoliTree
============================================

DESCRIPTION
--------------------------------------------

JoliTree réunit une feuille de style (CSS) et un JavaScript léger (2K minifié)
pour représenter un arbre en (X)HTML, avec dossiers repliables.

version :   1.0.1 - 2010-06-21
auteur:     nicolas Martin <joliclic@gmail.com>
site:       http://joliclic.free.fr/jsdev/jolitree
licence:    MIT license


CONTENU DE L'ARCHIVE:
--------------------------------------------

    - jolitree/
        |
        - jolitree.js : JavaScript non obfusqué
        - jolitree-min.js : JavaScript minifié (avec JSMin)
        - jolitree-packed.js : JavaScript compressé (Packer de Dean Edwards)
        - css/
            |
            - jolitree.css : feuille de style
            - jolitree-ie6.css : feuille de style pour IE6
            - jolitree-tango.css : feuille de style alternative
            - icons/ : images utilisées par jolitree.css
            - icons-gif/ : images utilisées par jolitree-ie6.css
            - icons-tango/ : images utilisées par jolitree-tango.css
    - doc.html : documentation de jolitree
    - doc-fr.html : documentation française de jolitree
    - example.html : un exemple html utilisant jolitree
    - readme.txt : ce fichier en anglais
    - readme-fr.txt : ce fichier


COMPATIBILITÉ:
--------------------------------------------

Doit fonctionner sur tous les Navigateurs modernes (Firefox, Opera, Safari,
Chrome,...).
Doit fonctionner sur IE6, IE7, IE8.

Le JavaScript utilisé est non-intrusif, si JavaScript est désactivé sur le
client l'arbre sera affiché statiquement, avec toutes les branches ouvertes.


UTILISATION
--------------------------------------------

Voir la documentation, doc.html. Et les sources de example.html.

La structure HTML utilisée pour représenter l'arbre ressemble au format
Netscape Bookmarks, elle est basée sur des listes de définition (<dl>, <dt> et
<dd>).

 - Le conteneur global est un élément <dl>, avec une classe "jolitree".
 - Un dossier est représenté par un <dd>, lequel contient un <p> qui représente
   son libellé, et un <dl> qui contient le contenu proprement dit du dossier.
 - Une simple entrée est un <dt> lequel peut éventuellement contenir un lien <a>.
 - Enfin, un séparateur est représenté par un <dd class="separator"> contenant
   lui-même un <hr>.

Voir les sources de example.html  pour un exemple complet

  Notes:
  ------
  - Vous devez ajouter la classe "last" à chaque élément (<dd> ou <dt>) qui est
    le dernier enfant d'un dossier, c'est nécessaire dans le cas où JavaScript
    n'est pas activé sur le client.
  - Si vous souhaitez utiliser une icône particulière pour une entrée, il suffit
    de mettre la classe "no-icon" sur le <dt> correspondant, celà supprimera
    l'icone par défaut. il ne vous reste plus qu'à ajouter une balise <img> dans
    le <dt>.
  - Et enfin, si vous souhaitez qu'un dossier soit ouvert par défaut lorsque le
    JavaScript est actif, ajouter lui la classe "opened" sur le <dd>
    correspondant. 

  Styles:
  -------
  - Pour la mise en forme, il suffit de lier la feuille de style jolitree.css à
    la page.
  - Une feuille alternative est disponible pour les anciennes versions
    d'Internet Explorer (IE6) qui ne comprennent pas la transparence des images
    png (elle utilise des gifs à la place).
    L'idéal est de lier les 2 feuilles à l'aide de commentaires conditionnels
    pour IE.
  - De nouveau, voir les sources de example.html pour un exemple complet.
  - Une autre feuille alternative est également disponible, jolitree-tango.css,
    basée sur le style Tango. Vous pouvez l'utiliser à la place de jolitree.css,
    ou créer la votre bien sur.

  Comportements:
  -------------
  - Pour les comportements de pliage/dépliage, il vous faut lier le fichier
    JavaScript jolitree.js, et créer une instance de la classe JoliTree avec
    l'élément <dl> souhaité en argument. 
  - Une fois encore, voir les sources de example.html pour un exemple complet.
  - Alternativement, vous pouvez utiliser à la place une version compressée.
    jolitree-min.js est une version minifiée (avec JSMin). jolitree-packed.js
    est compressé avec le Packer de Dean Edwards. Personnellement, je recommende
    d'utiliser la version minifiée, voir la version non compressée, car c'est un
    déjà un fichier léger ;) .


OUTILS EN RELATION
--------------------------------------------

Avec la dernière version de Boox, une extension pour Firefox, vous pouvez
facilement exporter un dossier particulier de vos marque-pages. Et avec le
convertisseur bm2jolitree vous pouvez facilement convertir un fichier de
marque-page en une structure adaptée à jolitree.

Ces outils sont disponibles sur mon site:

Boox:
http://joliclic.free.fr/mozilla/boox/

bm2jolitree:
http://joliclic.free.fr/jsdev/jolitree/#converter