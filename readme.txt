  JoliTree
============================================

DESCRIPTION
--------------------------------------------

JoliTree is a CSS Stylesheet and a lightweight JavaScript (2K minified) to
represent a (X)HTML tree, with collapsable folders.

version :   1.0.1 - 2010-06-21
author:     nicolas Martin <joliclic@gmail.com>
homepage:   http://joliclic.free.fr/jsdev/jolitree
license:    MIT license


CONTENT OF THE ARCHIVE:
--------------------------------------------

    - jolitree/
        |
        - jolitree.js : unobfuscated JavaScript
        - jolitree-min.js : minified JavaScript (using JSMin)
        - jolitree-packed.js : packed JavaScript (using Dean Edwards Packer)
        - css/
            |
            - jolitree.css : stylesheet
            - jolitree-ie6.css : stylesheet for IE6
            - jolitree-tango.css : alternative stylesheet
            - icons/ : images used by jolitree.css
            - icons-gif/ : images used by jolitree-ie6.css
            - icons-tango/ : images used by jolitree-tango.css
    - doc.html : documentation of jolitree
    - doc-fr.html : french documentation of jolitree
    - example.html : an html example using jolitree
    - readme.txt : this file
    - readme-fr.txt : this file in french


COMPATIBILITY:
--------------------------------------------

Should work on all modern Browsers (Firefox, Opera, Safari, Chrome,...).
Should work with IE6, IE7, IE8.

The JavaScript used is unobstrusive, if JavaScript is not enabled on the client
the tree will be displayed statically, all branches opened.


USAGE
--------------------------------------------

See the documentation, doc.html. And the source of example.html.

The HTML structure used to represent the tree looks like Bookmarks in Netscape
format, it is based on definition lists (<dl>, <dt>  and <dd>).

 - The global container is an <dl>, with a class "jolitree".
 - A folder is represented by a <dd>, which contains a <p> representing its
   label, and a <dl> that contains the actual content of this folder.
 - A simple entry is a <dt> which may optionally contain a link <a>.
 - Finally, a separator is represented by a <dd class="separator">, itself
   containing a <hr>.

See the source of example.html for a complete example.

  Notes:
  ------
  - You must add the class "last" to each element (<dd> or <dt>) which is the
    last child of a folder, it is necessary if JavaScript is not enabled on the
    client.
  - If you want to use a particular icon for an entry, just put the class
    "no-icon" on the corresponding <dt>, this removes the icon by default.
    Then, just add your <img> tag in the <dt>.
  - If you want a folder opened by default when JavaScript is enabled, add the
    class "opened" on the corresponding <dd>.

  Styles:
  -------
  - For the visual formatting, simply link the stylesheet jolitree.css to the
    page.
  - A alternative stylesheet is available to be compatible with the old versions
    of Internet Explorer (IE6), wich don't treat the PNG transparency. This
    stylesheet use GIF images rather than PNG.
    Ideally, link the 2 stylesheets with IE conditional comments
  - Again, see the source of example.html for a complete example.
  - Another alternative stylesheet is available, jolitree-tango.css, Tango style
    based. You can use it in place of jolitree.css, or create your own, of
    course.

  Behaviors:
  ----------
  - To enable the folding/unfolding behavior, you have to link the JavaScript
    file jolitree.js to your page, and create an instance of the JoliTree class
    with the cibled <dl> as argument.
  - One again, see the source of example.html for a complete example.
  - Alternatively, you can use instead a compressed version. jolitree-min.js is
    a minified version (with JSMin). jolitree-packed is compressed with the Dean
    Edwards JavaScript Packer. Personaly, I recommend to use the minified
    version, or the uncompressed version, because it's already a lightweight
    file ;) .


RELATED TOOLS:
--------------------------------------------

With the last version of Boox, a firefox extension, you can easily export a
single folder of yours bookmarks. And with the bm2jolitree converter you can
easily convert a bookmarks file into a jolitree structure.

All this tools are available on my site:

Boox:
http://joliclic.free.fr/mozilla/boox/en/

bm2jolitree:
http://joliclic.free.fr/jsdev/jolitree/en/#converter