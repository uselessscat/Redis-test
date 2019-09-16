
# Tutorial

Para inicializar el proyecto usar:

`docker run -it --rm -v ${PWD}/src:/src -w /src node:10.16.3-buster npm init`

luego, para instalar express.js

`docker run -it --rm -v ${PWD}/src:/src -w /src node:10.16.3-buster npm install express --save`


Crear app.js

Luego para correr el servidor de prueba ejecutar:

`docker run -itd -v ${PWD}/src:/src -w /src -p 3005:3000 node:10.16.3-buster node app.js`