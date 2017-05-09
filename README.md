# ProyectoGit
Trabajo de Git para Sistemas Informáticos DAW

<b> Preparando del Servidor </b>

Los repositorios se almacenarán en un servidor con acceso ssh, para el acceso se podrían crear cuentas por cada usuario pero si hay muchos usuarios esto se hace pesado. <br>
Para evitar esto se puede crear una única cuenta <b>git</b> a la que accederán todos los usuarios. Para acceder a esta cuenta por ssh se van a usar claves públicas y así no habrá que poner la contraseña siempre, para esto cada usuario genera una clave pública ( comando <i><b>ssh-keygen</b></i> en ~/.ssh) y se guardan todas en el directorio <i><b> ~/.ssh/authorized_keys </b></i> de la cuenta git del servidor.
<br><br>
Para más seguridad git trae un terminal que solo permite ejecutar funciones relacionadas con los repositorios. Se modifica el archivo /etc/passwd y al usuario git se le pone como terminal /usr/bin/git-shell, de esta forma solo podrá hacer acciones relacionadas con git por ssh.
<br><br>
Para crear los repositorios hay dos opciones:
<br><br>
Si se quiere crear uno vacio se puede crear manualmente la carpeta (En nuestro caso estarán en  /git)  y dentro se ejecuta <b>git --bare init</b>. Si se hace esto el primer usuario  tendrá que añadir crear un repositorio en su máquina y añadir el repositorio remoto con el comando <b><i>git remote add origin git@gitserver:/git/project.git</i></b>. Después de esto los demás usuarios podrán clonar el repositorio.
<br><br>
Si el repositorio se quiere subir a partir de un proyecto local que ya existe no hay más que copiarlo al servidor por ejemplo con <b><i>scp -r project.git git@gitserver:/git</i></b>, tras lo cual ya estará listo para clonar.
