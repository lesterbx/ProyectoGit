<h2>Uso Básico</h2>

<h4>1.	Configuración</h4>
Una vez instalado es importante configurar el nombre y email en git para poder identificar a los autores de los cambios que se hacen sobre un proyecto. Para ello, ejecutamos las siguientes instrucciones desde la terminal:

<b>git config --global user.name “Nombre”</b><br>
<b>git config --global user.email “<ejemplo@correo.com>”</b>

<h4>2.	Creación de un repositorio</h4>
En git, el contenido de un proyecto se guarda en un repositorio. Para iniciar un repositorio vacío, lo primero es situarse en la carpeta donde vamos a guardar dicho repositorio y ejecutar el siguiente comando: <b>git init</b><br>
Una vez ejecutado este comando se creará una carpeta con la extensión <b>.git</b>

Otra alternativa es clonar un repositorio que se encuentre en otra carpeta del ordenador o desde un sitio remoto para ello hay que ejecutar el comando <b>git clone</b> seguido de un parámetro que especifique la ubicación del repositorio que queremos clonar, por ejemplo: <b>git clone https://github.com/torvalds/linux</b>

<h4>3.	El directorio de trabajo</h4>
Es el sitio donde se crea el repositorio de git. Aquí se almacenan los archivos que esperamos añadir al repositorio en algún momento. 

<h4>4.	El staging index</h4>
Es un área temporal en el que añadimos archivos cuyos cambios estamos a punto de enviar a git en forma de commit.
Para añadir un archivo al staging index se utiliza el comando: <b>git add "nombre_archivo"</b>

Para examinar el staging index podemos utilizar el comando <b>git status.</b>

<h4>5.	Enviando cambios</h4>
Cuando se terminan de añadir cambios al staging index ya se puede hacer un commit. El commit confirma los cambios. El comando de confirmación es <b>git commit</b>
Al ejecutar el comando se abre el editor de texto del sistema operativo, donde se puede añadir un mensaje que describa los cambios.
Es recomendable añadir un mensaje que describa los cambios y responda a las siguientes preguntas:<br>
- ¿Por qué se han hecho los cambios?<br>
- ¿Qué cambios se han hecho?<br>
- ¿Qué consecuencias se espera de dicho cambio?

<h4>6.	Examinar el registro</h4>
Para visualizar el historial de commits basta con  ejecutar el comando  <b>git log</b>
Este comando presenta distintas opciones adicionales como: <b>git log --oneline --decorate --graph</b>

<h4>7. Eliminación de archivos</h4>
Para eliminar un archivo de Git, se debe eliminarlo del staging index y después confirmar. El comando <b>git rm</b> se encarga de eso. Previamente habrá que eliminar el archivo del directorio de trabajo. Si simplemente se elimina el archivo del directorio de trabajo, aparecerá bajo la cabecera “Modificados pero no actualizados” (“Changes not staged for commit”), es decir sin preparar.

<h4>8. Deshacer cambios</h4>
Para sacar un archivo del staging index ejecutamos el comando <b>git rest HEAD "nombre_archivo"</b>, de esta manera se evita que sea enviado en la siguiente confirmación. 

<h4>9.	Creación de ramas</h4>
El flujo de trabajo de git se basa en ramas. Una rama es una línea de desarrollo donde un commit sigue al anterior. Para crear una rama ejecutamos el siguiente comando: <b>git branch "nombre_rama"</b>
Para cambiar de ramas se ejecuta el comando: <b>git checkout</b>
Si vamos a crear una nueva rama y cambiar a ella podemos utilizar un solo comando: <b>git checkout -b "nombre_rama"</b>

<h4>10.	Borrar ramas</h4>
Para borrar una rama ejecutamos el comando: <b>git branch -d "nombre_rama"</b>

<h4>11.	Fusión de ramas</h4>
Para fusionar una rama dentro de otra ejecutamos el comando: <b>git merge "nombre_rama"</b>
Sin embargo a la hora de fusionar cambios pueden surgir conflictos, cuando esto sucede git añade unas marcas especiales en el archivo que queremos fusionar.

<h4>12.	Examinar commits</h4>
Para volver a un commit atrás en el tiempo podemos ejecutar el siguiente comando: <b>git checkout "código_commit"</b>

<h4>13. Push a repositorios remotos</h4>
Cuando el proyecto recibe cambios de muchas personas lo normal es establecer un repositorio central al que todos envían código. Para poder estar establecer un repositorio remoto podemos ejecutar el comando <b>git remote</b> seguido del nombre sel remoto y la dirección para acceder a ese remoto, por ejemplo: <b>git remote add origin https://github.com/usuario/proyecto.git</b>
Cuando se hace un clone de un remoto automaticamente ese repositorio se establece como remoto.
Una vez establecido el remoto podemos enviar cambios a dicho repositorio remoto mediante el comando <b>git push</b>, seguido del remoto al que queremos enviar cambios y la rama que queremos enviar, por ejemplo: <b>git push origin master</b>

<h4>14. Actualización de repositorios</h4>
Desde el punto de vista de git los repositorios remotos contienen otras ramas nuevas que son las remotas, por ejemplo si tenemos en nuestro ordenador tenemos una rama master en el repositorio remoto tendremos otra llamada origin/master. Podemos ver todas las ramas
incluidas las remotas ejecutamos el comando <b>git branch --all</b>. Con el comando <b>git pull origin master</b> podemos sincronizar cambios precedentes del repositorio origen.
