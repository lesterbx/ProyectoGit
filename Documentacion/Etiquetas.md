<h2>Creacion de Etiquetas o Tags</h2>

Los tags sirven para crear alias a commits concretos, de este modo en lugar de recordar un commit con su código podemos referirnos a él 
mediante una palabra que lo identifique de manera más fácil. Para crear una etiqueta se puede hacer mediante etiquetas ligeras o etiquetas 
anotadas.

<h4>- Etiquetas ligeras</h4>
 La creación de una etiqueta ligera se puede hacer ejecutando el comando <b>git tag "nombre_tag"</b>

<h4>- Etiquetas anotadas</h4>
 Las etiquetas anotadas son almacenadas como objetos completos en la base de datos de Git. Tienen suma de comprobación; contienen el 
 nombre del etiquetador, correo electrónico y fecha; tienen mensaje de etiquetado; y pueden estar firmadas y verificadas con GNU Privacy
 Guard (GPG). Generalmente se recomienda crear etiquetas anotadas para disponer de toda esta información. Para crear este tipo de etiquetas
 se debe ejecutar el comando <b>git tag -a "nombre_tag"</b>.
 Tras ejecutar este comando git lanza un editor para poder describir la etiqueta.  Si no queremos que dicho editor aparezca se ejecuta el
 comando con la opción -m seguido se un mensaje corto, asi: <b>git tag -a "nombre_tag" -m "mensaje"</b>
 
<h4>Examinar etiquetas</h4>
Para poder examinar una etiqueta creada podemos ejecutar el comando <b>git show "nombre_tag"</b>

Para poder etiquetar más tarde un commit, basta con ejecutar el comando anterior especificando el número de commit al que se quiere 
etiquetar: <b>git tag -a "nombre_tag" -m "mensaje" "código_commit"</b>
