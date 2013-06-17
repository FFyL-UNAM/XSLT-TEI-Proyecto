# Proyecto XSLT TEI

Proyecto de [filos.unam.mx](http://www.filos.unam.mx) para generar libros electrónicos a partir de la formación de documentos en Microsoft Word, que surgen de proyectos de investigación realizados en la Facultad de Filosofía y Letras, UNAM.


## Cómo empezar

Descargar las [XSL stylesheets for TEI XML](http://www.tei-c.org/Tools/Stylesheets) para poder transformar documentos

    svn co https://tei.svn.sourceforge.net/svnroot/tei/trunk/  /path/to/local/directory/

Instalar los comandos de transformación como **docxtotei**, **teitoepub3**, etc.

    cd /path/to/local/directory/Stylesheets && sudo make install

Finalmente, clonar este repositorio a los perfiles de transformación

    sudo git clone git@github.com:FFyL-UNAM/XSLT-TEI-Proyecto.git /usr/share/xml/tei/stylesheet/profiles/[nombredelperfil]


## Cómo usar

Generar un documento XML de un documento de Microsoft Word

    docxtotei --profile=[nombredelperfil] file.docx tei.xml

Generar un libro electrónico en formato ePub desde un documento XML

    teitoepub3 --profile=[nombredelperfil] tei.xml book.epub


### Más información

* [Proyecto TEI](http://proyectotei.wordpress.com)
* [Dropbox](https://www.dropbox.com/sh/s2d5twwe9y2d35q/viI4mmtcZE)

