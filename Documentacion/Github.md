<h2>GitHub</h2>

En github se trabaja igual que con otro servidor de git.
<br><br>
Para añadir claves ssh hay que generarla con el comando <b>ssh-keygen -t rsa -b 4096 -C "your_email@example.com"</b>
Luego se añade en los ajustes de la cuenta en la sección correspondiente.
<br><br>
En GitHub para poder hacer push sobre un proyecto el dueño del mismo tiene que añadirte como colaborador, 
por lo que si se quieren hacer cambios sobre un proyecto ajeno hay que hacer un <b>fork</b>, que no es más que una copia del proyecto
en nuestro propio repositorio. <br>
Una vez hechos los cambios y si se considera que vendría bien añadirlos al proyecto original se hace un <b>pull request</b>, 
que es una petición que llegará al propietario del proyecto para que incluya los cambios si lo cree conveniente.
