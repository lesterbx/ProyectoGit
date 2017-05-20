Ramas
Una rama Git es simplemente un apuntador móvil apuntando a una de esas confirmaciones (commits). La rama por defecto de Git es la rama 
master. Con la primera confirmación de cambios que realicemos, se creará esta rama principal master apuntando a dicha confirmación. 
En cada confirmación de cambios que realicemos, la rama irá avanzando automáticamente. Y la rama master apuntará siempre a la última 
confirmación realizada.
 
Cuando se crea una rama nueva lo que en realidad se crea es un nuevo apuntador apuntando a la misma confirmación donde estés actualmente.
 
Git sabe en qué rama se está en cada momento mediante un apuntador especial denominado HEAD
 
Para saltar de una rama a otra, utilizariamos el comando git checkout testing (en este caso).
 

