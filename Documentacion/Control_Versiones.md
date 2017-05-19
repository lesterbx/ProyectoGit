<h2> Control de versiones </h2>
El control de versiones es un sistema que registra los cambios que se hacen sobre un archivo o conjunto de archivos, de forma que se pueda volver a un estado anterior de los archivos en cualquier momento.
Lo que más usaremos son archivos de código, pero el control se puede ralizar sobre cualquier tipo de archvos (texto, diseño).

El control de versiones más básico que se puede hacer es algo manual, por ejemplo ir guardando los archivos en distintas carpetas, pero esto es un método muy propenso a tener errores, por lo que hace mucho que aparececieron herramientas que facilitan el control.

<h4>Sistemas Locales</h4>
Es una base de datos local que registra todos los cambios que se van haciendo a los archivos, una herramienta popular fue <b>rcs</b>, que permite gestionar archivos individuales por un solo usuario y almacena únicamente las diferencias entre archivos.
<br>
<img src="https://git-scm.com/figures/18333fig0101-tn.png">

<h4>Sistemas Centralizados</h4>
Permiten la colaboración entre varios usuarios, ya que la base de datos con los archivos versionados se sitúa en un servidor, de dónde se los descargan los clientes. Tiene ventajas claras sobre los sitemas locales, ya que permite saber hasta cierto punto en que trabajan los demás y es más fácil de administrar que un repositorio para cada desarrollador.
<br>
<img src="https://git-scm.com/figures/18333fig0102-tn.png"/>

Pero estos sistemas también tiene desventajas, como que todas las decisiones importantes tienen que ser aprobadas por el responsable, o que al estar la información en un solo sitio es posible que se quede inaccesible algún tiempo o que se pierda o se corrompa si no se tienen copias de seguridad adecuadas.
La herramienta más conocida de este tipo es Subversion (<b>svn</b>)

<h4>Sistemas Distribuidos</h4>
En los sistemas distribuidos los clientes no descargan solo la última revisión o archivos concretos, si no que tienen una copia local completa de todos los datos del repositorio, así si el servidor se cae o se daña basta con recuperar los datos de algún usuario. Esta forma de trabajo también facilita el usar varios repositorios a la vez.
<br>
<img src="https://git-scm.com/figures/18333fig0103-tn.png"/>

Algunos de estos sistemas son Mercurial o <b>Git</b>.
