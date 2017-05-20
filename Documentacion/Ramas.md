<h2>Ramas</h2>

Una rama Git es simplemente un apuntador móvil apuntando a una de esas confirmaciones (commits). La rama por defecto de Git es la rama 
master. Con la primera confirmación de cambios que realicemos, se creará esta rama principal master apuntando a dicha confirmación. 
En cada confirmación de cambios que realicemos, la rama irá avanzando automáticamente. Y la rama master apuntará siempre a la última 
confirmación realizada.<br>
<img src="https://git-scm.com/figures/18333fig0303-tn.png"><br>

Cuando se crea una rama nueva lo que en realidad se crea es un nuevo apuntador apuntando a la misma confirmación donde estés actualmente.<br>
<img src="https://git-scm.com/figures/18333fig0304-tn.png"><br>

Git sabe en qué rama se está en cada momento mediante un apuntador especial denominado HEAD.<br>
<img src="https://git-scm.com/figures/18333fig0305-tn.png"><br>

Para saltar de una rama a otra, utilizariamos el comando git checkout testing (en este caso).<br>
<img src="https://git-scm.com/figures/18333fig0306-tn.png">

