Para pisar estilos de la libreria de bootstrap las opciones son :

-Ser mas especfico en la etiqueta
-Colocar el link reference de nuestro css por debajo
-Extraer la etiqueta desde el inspector y normalizarla (llevar a 0 los valores que no queremos que bootstrap modifique).

-Para las secciones de tarjetas usar la clase row dentro de la section con la clase container
y despues se le asigna cuando ocupan de las columnas (ej : col-md-4)

-Utilizar el sistema de grillas para hacer la parte de las cards en receipes 
y en el index.

rem : esta atado al root del navegador o la root 
em : de la etiqueta padre (puede ser la de HTML)

Usar los container de bootstrap,tipografia, la parte de utilities.

PseudoClases
Palabra clave que se añade a selectores que especifica un estado especial del elemento seleccionado. Permite dar estilo no solo en relacion al DOM sino tambien a factores externos.
Ej: Checked para algunos elementos del form
 sino tambien :target :active

A una etiqueta de las checkbox se le puede poner la etiqueta :chequed

nth-of-type te sirve para diferencian elementos dentro de una lista para poder darle estilos especificos
