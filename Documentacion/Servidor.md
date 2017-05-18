<h1>Preparando el Servidor</h1>

Los repositorios se almacenarán en un servidor con acceso ssh, para el acceso se podrían crear cuentas por cada usuario pero si hay muchos usuarios esto se hace pesado. 
Para evitar esto se puede crear una única cuenta git a la que accederán todos los usuarios. Para acceder a esta cuenta por ssh se van a usar claves públicas y así no habrá que poner la contraseña siempre, para esto cada usuario genera una clave pública ( comando <b>ssh-keygen</b> en <b>~/.ssh</b>) y se guardan todas en el directorio <b>~/.ssh/authorized_keys</b> de la cuenta git del servidor. 

Para más seguridad git trae un terminal que solo permite ejecutar funciones relacionadas con los repositorios. Se modifica el archivo <b>/etc/passwd</b> y al usuario git se le pone como terminal <b>/usr/bin/git-shell</b>, de esta forma solo podrá hacer acciones relacionadas con git por ssh. 

Para crear los repositorios hay dos opciones: 

Si se quiere crear uno vacio se puede crear manualmente la carpeta (En nuestro caso estarán en /git) y dentro se ejecuta <b>git --bare init</b>. Si se hace esto el primer usuario tendrá que añadir crear un repositorio en su máquina y añadir el repositorio remoto con el comando <b>git remote add origin git@gitserver:/git/project.git </b>. Después de esto los demás usuarios podrán clonar el repositorio. 

Si el repositorio se quiere subir a partir de un proyecto local que ya existe no hay más que copiarlo al servidor por ejemplo con <b>scp -r project.git git@gitserver:/git</b>, tras lo cual ya estará listo para clonar.
