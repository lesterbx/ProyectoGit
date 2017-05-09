# ProyectoGit
Trabajo de Git para Sistemas Informáticos DAW

<b> Preparación del Servidor </b>

Los repositorios se almacenarán en un servidor con acceso ssh, para el acceso se podrían crear cuentas por cada usuario, pero si hay muchos usuarios esto se hace pesado. 
Para evitar esto se puede crear una única cuenta <b>git</b> a la que accederán todos los usuarios. Para acceder a esta cuenta  por ssh se pueden usar claves públicas y así no habrá que poner la contraseña siempre, para esto cada usuario genera una clave pública y se guardan todas en el archivo  <i> ~/.ssh/authorized_keys </i> de la cuenta git.
