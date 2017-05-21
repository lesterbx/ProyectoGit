<h2> Repositorios Remotos </h2>

Son versiones del proyecto que se encuentran alojados en algún punto de la red. Se pueden tener varios, y se pueden tener acceso de lectura/escritura o sólo lectura, según las necesidades.
<br><br>
Para obtener una copia de un repositorio remoto se utiliza el comando <b> git clone </b> seguido de la dirección del repositorio. Se puede obtener por varios protocolos, como http, ssh o git. 
<br><br>
Para ver los repositorios que tenemos configurados se utiliza <b> git remote </b>, que puede ir seguido de la opción <b> -v </b> para que muestre también la url de cada repositorio remoto. Por defecto se tiene uno llamado <b>origin</b> que es de dónde se clonó el repositorio inicialmente.
<br><br>
Para añadir un repositorio remoto se utiliza el comando <b> git remote add </b> seguido del nombre que se le quiera dar y la url del repositorio.
<br><br>
<b><i> git remote add test git@gitserver:/git/project.git </i></b>
<br><br>
Si se quiere obtener información de lo que está en el repositorio remoto se utiliza <b> git fetch </b>, esto recupera los datos que no se tengan todavía, pero no une la información con tu trabajo ni se modifica en lo que estás trabajando, para eso se utiliza el comando <b> git pull </b>, esto hará que se recuperé la información del repositorio y automátimanete intente fusionar la rama remota con la rama local.
<br><br>
<b><i> git pull origin master </i></b>
<br><br>
Para compartir tu trabajo con el repositorio remoto se utiliza el comando <b> git push </b> seguido del repositorio y la rama que se quiere compartir, para esto hay que tener permiso de escritura en el servidor. Si la versión del servidor contiene cambios que la tuya no tiene no te dejará compartir la tuya, primero tendrás que bajar la versión remota, incorporarla a la tuya y ya después podrás subirla.
<br><br>
También se puede ver más información de un repositorio con el comando <b> git remote show </b> y el nombre del repositorio. Est dará información de las ramas del repositorio y de como se relacionan con tus ramas locales.
<br><br>
Por último se pueden renombrar los repositorios con <b> git remote rename </b> y se pueden eliminar con <b> git remote rm </b>.

<h3>Ramas Remotas</h3>

Son copias locales que hacen referencia al el estado de las ramas en los repositorios remotos, y se actualizan automáticamente  al conectarse con ellos. Se suelen referenciar como <b><i>(remoto)/(rama)</i></b>. Al clonar un repositorio git crea tu rama <b>master</b> y la rama <b>origin/master</b> que apunta a la rama <b>master</b> del repositorio <b>origin</b>. De forma que los registros pueden avanzar de forma distinta. 
<br>
<img src="https://git-scm.com/figures/18333fig0323-tn.png">
<br><br>
Esto también permite tener varios servidores con ramas distintas, por ejemplo para distintos equipos de desarrollo. 
<br><br>
Cuando se hace push sobre una rama remota lo que hace git es sustituir la rama remota por tu rama local, por eso obliga a tener todos los cambios que se hayan hecho en el repositorio.
<br><br>
Para trabajar con las ramas remotas se pueden fusionar con alguna rama local, pero lo habitual es tener ramas de seguimiento, que son ramas que tienen una relación directa con alguna rama del repositorio remoto, por lo que al hacer <b>pull</b> sobre ellas recupera las referencias remotas y las fusiona(merge) con la rama local correspondiente. La rama master por defecto es una rama de seguimiento de origin/master.
<br><br>
Para eliminar una rama remota se puede hacer con <b> git push [repositorio] --delete [nombre_rama] </b>






