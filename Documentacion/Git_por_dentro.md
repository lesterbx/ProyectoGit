<h2>Git por dentro</h2>

Git es un sistema de archivos almacenados por clave - valor, esto quiere decir que almacena objetos que se identifican con una clave única.
<br><br>
Los objetos que almacena son de varios tipos:

- <b>Tree</b>: Se corresponde con directorios, puede contener otros objetos tipo tree o tipo blob, asi como sus nombres.
- <b>Blob</b>: Se corresponde con el contenido de un archivo, no almacena el nombre.
<br>
<img src="https://git-scm.com/book/en/v2/images/data-model-1.png">
<br>

- <b>Commits</b>: Almacenan cada commit que se hace, contiene el tree de la carpeta raíz del proyecto en ese momento, también hace referencia al commit anterior (parent), y guarda quien hizo el commit, cuando y un mensaje que lo describa.

<br>
<img src="https://git-scm.com/book/en/v2/images/data-model-3.png">
<br>

Los objetos son permanentes, y se almacenan en la carpeta objects dentro de .git. <br>
Para almacenarlos primero crea una cabezera que contiene el tipo de archivo y su tamaño seguido de un byte nulo. Por ejemplo:<br><br>
Contenido: <i><b>"what is up, doc?"</b></i>
<br>
Cabecera: <i><b>"blob 16\u0000"</b></i>
<br><br>
Luego concatena la cabezera con el contenido del archivo y calcula el checksum utilizando SHA-1, esto devuelve un hash de 40 caracteres hexadecimales.<br><br>
<i><b>"blob 16\u0000what is up, doc?" => "bd9dbf5aae1a3862dd1526723246b20206e5fc37" </b></i>
<br><br>
Después coge el resultado y lo comprime utilizando la librería zlib:<br><br>
<i><b>"x\x9CK\xCA\xC9OR04c(\xCFH,Q\xC8,V(-\xD0QH\xC9O\xB6\a\x00_\x1C\a\x9D"</b></i>
<br><br>
Este es el contenido que se guardará en el disco, y se guardará en una carpeta llamada como los dos primeros caracteres del sha-1 y en un fichero llamado como los 38 restantes:<br><br>
<i><b>".git/objects/bd/9dbf5aae1a3862dd1526723246b20206e5fc37"</b></i>
<br><br>
Git permite ver cualquier objeto de forma entendible con el comando <b>git cat-file -p</b> seguido del checksum del objeto.
<br><br>
También existen los objetos de tipo etiqueta, que contienen el checksum de un comit determinado, así como quien la creo cuando y un mensaje descriptivo. Se almacenan en la carpeta <b><i>.git/refs/tags</i></b>.
<br><br>
Las ramas se guardan en la carpeta <b><i>.git/refs/heads/</i></b>, y no son más que archivos con el nombre de la rama y que contienen el commit al que apuntan.
<br><br>
También está el archivo HEAD que referencia al archivo de la rama en la que se encuentra y el directorio remotes donde se guardan las ramas remotas.

