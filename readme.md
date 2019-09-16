
# Tutorial

## Iniciar el proyecto
Para inicializar el proyecto usar:

`docker run -it --rm -v ${PWD}/src:/src -w /src node:10.16.3-buster npm init`

luego, para instalar express.js

`docker run -it --rm -v ${PWD}/src:/src -w /src node:10.16.3-buster npm install express --save`


Crear app.js con

``` js
var express = require('express');
var app = express();

app.get('/', function (req, res) {
  res.send('Hello World!');
});

app.listen(3000, function () {
  console.log('Example app listening on port 3000!');
});
```

Luego para correr el servidor de prueba (en el puerto 3005) ejecutar:

`docker run -itd -v ${PWD}/src:/src -w /src -p 3005:3000 node:10.16.3-buster node app.js`

Detener el contenedor luego de ver el _Hello world_ en el navegador

## Configurar servicios

Configurar luego docker compose. Ver `docker-compose.yml`.

## Instalar dependencias

Instalar el cliente de redis:

`docker run -it --rm -v ${PWD}/src:/src -w /src node:10.16.3-buster npm install redis`