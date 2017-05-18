<h2>Configuración</h2>
La configuración de git se hace con el comando <b>git config</b>, la única configuración obligatoria es la del usuario y el email:
<br><br><b><i>
 git config --global user.name "John Doe"<br>
 git config --global user.email johndoe@example.com<br><br>
</i></b>
Pero estas no son las únicas configuraciones posibles, hay muchas otras opciones que permiten personalizar el uso de git, para esto 
existen varios archivos de configuración en los que git buscará las opciones.<br><br>
- El primero es <b>/etc/gitconfig</b>, aqui se guarda la configuración que es común 
a todos los usuarios del sistema. Git utilizará este archivo cuando se le pase la opción <b>--system</b> a <b>git config</b>.<br>
- El siguiente archivo en el que buscará  es <b>~/.gitconfig</b> (o <b>~/.config/git/config</b>), aqui se guarda la configuración propia de cada usuario,
se utiliza con la opción <b> --global </b>.<br>
- Por último buscara dentro del propio repositorio en el fichero <b>.git/config</b>, y será la configuración del repositorio.<br>
<br>
La configuración de cada nivel sobreescribe a la del anterior
