<h2> Repositorios Remotos </h2>

Son versiones del proyecto que se encuentran alojados en algún punto de la red. Se pueden tener varios, y se pueden tener acceso de lectura/escritura o sólo lectura, según las necesidades.
<br>
Para obtener una copia de un repositorio remoto se utiliza el comando <b> git clone </b> seguido de la dirección del repositorio. Se puede obtener por varios protocolos, como http, ssh o git. 
<br> 
Para ver los repositorios que tenemos configurados se utiliza <b> git remote </b>, que puede ir seguido de la opción <b> -v </b> para que muestre también la url de cada repositorio remoto. Por defecto se tiene uno llamado <b>origin</b> que es de dónde se clono el repositorio inicialmente.
<br>
Para añadir un repositorio remoto se utiliza el comando <b> git remote add </b> seguido del nombre que se le quiera dar y la url del repositorio.
<br>
<b><i> git remote add test git@gitserver:/git/project.git </i></b>
<br>
<br> Si se quiere obtener información de lo que está en el repositorio remoto se utiliza <b> git fetch </b>, esto recupera los datos que no se tengan todavía, pero no une la información con tu trabajo ni se modifica en lo que estás trabajando, para eso se utiliza el comando <b> git pull </b>, est hará que se recuperé la información del repositorio y automátimanete intente fusionar la rama remota con la rama local.
<br>
<b><i> git pull origin master </i></b>
<br>
Para compartir tu trabajo con el repositorio remoto se utiliza el comando <b> git push </b> seguido del repositorio y la rama que se quiere compartir, para esto hay que tener permiso de escritura en el servidor. Si la versión del servidor contiene cambios que la tuya no tiene no te dejará compartir la tuya, primero tendrás que bajar la versión remota, incorporarla a la tuya y ya después podrás subirla.
<br>
También se puede ver más información de un repositorio con el comando <b> git remote show </b> y el nombre del repositorio. Est dará información de las ramas del repositorio y de como se relacionan con tus ramas locales.
<br>
Por último se pueden renombrar los repositorios con <b> git remote rename </b> y se pueden eliminar con <b> git remote rm </b>.


