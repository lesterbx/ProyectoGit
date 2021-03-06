<h2>Git</h2>
<ul>
<li>Es un sistema de control de versiones distribuido. </li>
<li>No depende de acceso a la red o un repositorio  central. </li>
<li>Enfocado a la velocidad, uso práctico y manejo de  proyectos grandes.</li>
<li>Creado por Linus Torvalds, el creador del núcleo  Linux.</li>
<li>No hay una copia original del código del proyecto, solo existen las distintas copias de trabajo. </li>
<li>Operaciones como los commits, mirar el historial o rehacer cambios, no necesitan de una conexión con un servidor central, esta conexión solo es necesaria al “compartir” tu rama con otro cliente del sistema. </li>
<li>Cada copia de trabajo es una copia remota del código fuente y de la historia de cambios, dando una seguridad muy natural contra la pérdida de los datos.</li>
</ul>

Git modela sus datos como un conjunto de instantáneas(snapshots) de un mini sistema de archivos. Cada vez que confirmas un cambio, o guardas el estado de tu proyecto en Git, él básicamente hace una foto del aspecto de todos tus archivos en ese momento, y guarda una referencia a esa instantánea.

Git tiene tres estados principales en los que se pueden encontrar tus archivos: <b>modificado</b> (modified), <b>preparado</b> (staged) y <b>confirmado</b> (committed). Modificado significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos. Preparado significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación. Confirmado significa que los datos están almacenados de manera segura en tu base de datos local.

<img src="https://git-scm.com/figures/18333fig0106-tn.png">

El flujo de trabajo básico en Git es algo así:

<ul>
<li>Modificas una serie de archivos en tu directorio de trabajo.</li>
<li>Preparas los archivos, añadiendolos a tu área de preparación.</li>
<li>Confirmas los cambios, lo que toma los archivos tal y como están en el área de preparación, y almacena esas instantáneas de manera permanente en tu directorio de Git.</li>
</ul>
