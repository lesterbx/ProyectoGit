# ProyectoGit
Trabajo de Git para Sistemas Informáticos DAW

<b> Preparación del Servidor </b>

Los repositorios se almacenarán en un servidor con acceso ssh, para el acceso se podrían crear cuentas por cada usuario pero si hay muchos usuarios esto se hace pesado. <br>
Para evitar esto se puede crear una única cuenta <b>git</b> a la que accederán todos los usuarios. Para acceder a esta cuenta por ssh se van a usar claves públicas y así no habrá que poner la contraseña siempre, para esto cada usuario genera una clave pública ( comando <i><b>ssh-keygen</b></i> en ~/.ssh) y se guardan todas en el directorio <i><b> ~/.ssh/authorized_keys </b></i> de la cuenta git del servidor.
<br><br>
Una vez creados los usuarios hay que crear el repositorio, esto hay que hacerlo manualmente, desde el propio servidor o ssh, nosotros los haremos en <b>/git</b>, se crea la carpeta del repositorio que tiene que acabar en .git y estando dentro se ejecuta <b>git --bare init</b> para inicializar un repositorio vacío, el propietario tiene que ser la cuenta git.
<br><br>
Para más seguridad git trae un terminal que solo permite ejecutar funciones relacionadas con los repositorios. Se modifica el archivo /etc/passwd y al usuario git se le pone como terminal /usr/bin/git-shell, de esta forma solo podrá hacer acciones relacionadas con git por ssh.
