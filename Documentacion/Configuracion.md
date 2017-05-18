<h2>Configuración</h2>
La configuración de git se hace con el comando <b>git config</b>, la única configuración obligatoria es la del usuario y el email:
<br><br>
<b><i>
 git config --global user.name "John Doe"<br>
 git config --global user.email johndoe@example.com<br><br>
</i></b>
Pero estas no son las únicas configuraciones posibles, hay muchas otras opciones que permiten personalizar el uso de git, para esto 
existen varios archivos de configuración en los que git buscará las opciones.<br><br>
- El primero es <b>/etc/gitconfig</b>, aqui se guarda la configuración que es común 
a todos los usuarios del sistema. Git utilizará este archivo cuando se le pase la opción <b>--system</b> a <b>git config</b>.<br>
- El siguiente archivo en el que buscará  es <b>~/.gitconfig</b> (o <b>~/.config/git/config</b>), aqui se guarda la configuración propia de cada usuario,
se utiliza con la opción <b> --global </b>.<br>
- Por último buscara dentro del propio repositorio en el fichero <b>.git/config</b>, y será la configuración del repositorio.<br>
<br>
La configuración de cada nivel sobreescribe a la del anterior. Las opciones pueden ser para cliente o para servidor, aquí veremos las más importantes<br>

<h3>Opciones de Cliente</h3>

- <b>core.editor</b>: Editor de texto para los mensajes, por defecto será el del sistema, o vi si no hay.
- <b>commit.template</b>: Ruta de un fichero que se utilizará como plantilla para los mensajes.
- <b>core.pager</b>: Paginador cuando se muestra información muy larga, por defecto less.
- <b>core.excludesfile</b>: Ruta de un fichero que contenga las reglas globales para ignorar archivos.
- <b>help.autocorrect</b>: Si se pone a 1, git ejecutará automáticamente comandos aunque estén mal escritos.
- <b>color.ui</b>: Modificar como se colorean las salidas, por defecto se colorea si es un terminal pero no a tuberías o ficheros. También se puede elegir por separado cada elemento a colorear (branch, diff status) y los colores que se quieren ( <i>git config -- global color.diff.meta "blue black bold"</i>).

También se pueden usar herramientas externas para hacer <b>merge</b> o para <b>diff</b>, esto se configura con:
- merge.tool 
- mergetool.tool.cmd
- mergetool.tool.trustExitCode
- diff.external
