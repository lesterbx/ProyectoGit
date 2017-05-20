<h2>Uso Básico</h2>

<h4>1.	Configuración</h4>
Una vez instalado es importante configurar el nombre y email en git para poder identificar a los autores de los cambios que se hacen sobre un proyecto. Para ello, ejecutamos las siguientes instrucciones desde la terminal:

<h4>git config --global user.name “Nombre”

git config --global user.email “<ejemplo@correo.com>” </h4>

<h4>2.	Creación de un repositorio</h4>
En git, el contenido de un proyecto se guarda en un repositorio. Para iniciar un repositorio vacío, lo primero es situarse en la carpeta donde vamos a guardar dicho repositorio y ejecutar el siguiente comando:<h4>git init</h4>
Una vez ejecutado este comando se creará una carpeta con la extensión <h4>.git.</h4>

Otra alternativa es clonar un repositorio que se encuentre en otra carpeta del ordenador o desde un sitio remoto para ello hay que ejecutar el comando <h4>git clone</h4> seguido de un parámetro que especifique la ubicación del repositorio que queremos clonar, por ejemplo: <h4>git clone https://github.com/torvalds/linux</h4>

<h4>3.	El directorio de trabajo<h4>
Es el sitio donde se crea el repositorio de git. Aquí se almacenan los archivos que esperamos añadir al repositorio en algún momento. 

<h4>4.	El staging index</h4>
Es un área temporal en el que añadimos archivos cuyos cambios estamos a punto de enviar a git en forma de commit.
Para añadir un archivo al staging index se utiliza el comando: <h4>git add "nombre_archivo"</h4>

Para examinar el staging index podemos utilizar el comando <h4>git status.</h4>

<h4>5.	Enviando cambios</h4>
Cuando se terminan de añadir cambios al staging index ya se puede hacer un commit. El commit confirma los cambios. El comando de confirmación es <h4>git commit</h4>
Al ejecutar el comando se abre el editor de texto del sistema operativo, donde se puede añadir un mensaje que describa los cambios.
Es recomendable añadir un mensaje que describa los cambios y responda a las siguientes preguntas:
- ¿Por qué se han hecho los cambios?
- ¿Qué cambios se han hecho?
- ¿Qué consecuencias se espera de dicho cambio?

