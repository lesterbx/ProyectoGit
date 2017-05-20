<h2>Git</h2>
-<b></b>Es un sistema de control de versiones distribuido. 
-No depende de acceso a la red o un repositorio  central. 
-Enfocado a la velocidad, uso práctico y manejo de  proyectos grandes.
-Creado por Linus Torvalds, el creador del núcleo  Linux.
-No hay una copia original del código del proyecto, solo existen las distintas copias de trabajo. 
-Operaciones como los commits, mirar el historial o rehacer cambios, no necesitan de una conexión con un servidor central, esta conexión solo es necesaria al “compartir” tu rama con otro cliente del sistema. 
-Cada copia de trabajo es una copia remota del código fuente y de la historia de cambios, dando una seguridad muy natural contra la pérdida de los datos.

Git modela sus datos como un conjunto de instantáneas(snapshots) de un mini sistema de archivos. Cada vez que confirmas un cambio, o guardas el estado de tu proyecto en Git, él básicamente hace una foto del aspecto de todos tus archivos en ese momento, y guarda una referencia a esa instantánea.

Git tiene tres estados principales en los que se pueden encontrar tus archivos: <b>confirmado</b> (committed), <b>modificado</b> (modified), y <b>preparado</b> (staged). Confirmado significa que los datos están almacenados de manera segura en tu base de datos local. Modificado significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos. Preparado significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.

<img src="https://git-scm.com/figures/18333fig0106-tn.png">

El flujo de trabajo básico en Git es algo así:

-Modificas una serie de archivos en tu directorio de trabajo.
-Preparas los archivos, añadiendolos a tu área de preparación.
-Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación, y almacena esas instantáneas de manera permanente en tu directorio de Git.

