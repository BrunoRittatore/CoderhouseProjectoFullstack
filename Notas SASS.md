Notas Clases SASS I y SASS II

SASS I

Utilizar los comandos del NPM para instalar los node modules correspondientes a SASS y meter en el gitignore la carpeta para que no la suba al repositorio

Se carga en la parte de scripts el build css para que los archivos de tipo scsss los agarre de una carpeta y los convierta en css, no se tiene que poner el nombre de css igual al nombre que ya tiene el archivo original por que los atributos se van a pisar todos por lo que se traduzca de los scss


Despues se tienen que pasar todo el css que se quiere pasar a SASS y anidar

Una vez anidado se corre el comando "npm run build-css" que es el comando que esta en el apartado de scripts del package json

Se instala nodemon para que se encargue de hacer watch en los archivos scss para que el build lo traduzca al css

Para utilizar Sass previamente tengo que organizar en una carpeta de vistas a las paginas de html 
luego en la carpeta de scss realizar una carpeta de vistas con cada scss de los htmls

Basicamente ir encarpeta segun la conveniencia

![ScreenShot](/orden%20carpetas.png)

- A normalize va todo lo relacionado al css que resetea la web
-variables todo lo relacionado a la root
-la carpeta partials incluye lo del footer y el header

En el index.scss se tiene que importar mediante las rutas los archivos scss de cada vista/partial

-El TRANSLATE ES UN ARCHIVO TEMPORAl , una vez que esta todo traducido al css lo que estaba en el index se puede pisar mediante el package json cambiando la ruta de destino del traslate



NOTAS SASS II 

las variables se nombran con $ y tienen que ser reemplazadas en todos los archivos intermedios de sass para que los tome correctamente al momento de traducir

Se ve bucles 
sintaxis :
Para decirle a sass que quiero usar esa variable dentro del bucle utilizo el numeral

@for $i from 1 trough 10 {

    .col-#{$i}{
        width: 10% * $i; 
    }
}
Este codigo lo que va a hacer es que desde el col-1 va a ir variando el width

Estructura de EACH
Es similar a lo que es un map en JS 
@each $animal in perro,zorro,guacamayo {
    .card__img--#{animal} {
        height :300px
        backgroudd-image: url ('../img/..') 

    }

}

Estructura de MAPS 

$redes : (
    twitter: white;  
    facebook : blue;
    send-mail : red;
)
Creamos un bucle para usar los valores del mapa 

@each $red, $color  in $redes {
    .btn--#{$red}{
        background-color : $color;
    }

}


despues se tiene que usar un map-get para llamarla desde algun atributo


EXTEND : Se utiliza el extend para traer los estilos de una clase a otra

MIXINS 
Permiten definir estilos que pueden ser reutilizado en el proyecto, a diferencia con extend es que los mixins puede recibir argumentos , los cuales permiten producir gran variedad de stilos con un par de lineas.

Declaración :

@mixin sizes ($width,%height) {
    height : $height;
    width  : $width;
}
.box {
    @include sizes(valorde width,valor height)
}

Siempre hay que completar los valores , en caso de no tener hay que poner el que trae por defecto el atributo o cambiar el tipo de mixin que se usa


