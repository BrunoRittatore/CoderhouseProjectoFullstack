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
