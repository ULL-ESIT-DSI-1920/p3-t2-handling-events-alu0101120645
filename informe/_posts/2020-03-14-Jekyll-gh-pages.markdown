---
layout: post
title:  "Jekyll y Github-Pages"
date:   2020-03-14 20:55:19 +0000
categories: jekyll update
---
##### Jekyll y Github-Pages

Para la instalacion de Jekyll deberemos de tener en cuenta que version de ruby tenemos instalada en nuestra maquina, debido a que hay versiones que da problemas.

La practica he usado tres versiones y la unica que he conseguido que me funciones es con la versión [2.3.0].

- Para comenzar con el uso de esta herramienta comenzaremos con un `bundle init`

- Una vez generado el Gemfile le añadiremos ` gem 'github-pages', group: :jekyll_plugins`

- Realizaremos un `bundle install` para instalar Jekyll

- Ahora usaremos el comando `gem install jekyll`

- Crearemos un directorio con `jekyll new`

- Entraremos en el directorio creado y pondremos `nmp init`

- Instaleremos el modulo de gh-pages: `nmp i gh-pages`

- Deberemos de añadir la siguiente linea al archivo package.json que se nos creo anteriormente `"deploy":"gh-pages -d _site"`

Quedara de la siguiente manera

```Javascript
{
  "name": "informe",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "deploy":"gh-pages -d _site",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "gh-pages": "^2.2.0"
  }
}
```

- Se crea el site con bundle exec jekyll build y luego se ejecuta el comando npm run deploy, de esta manera ya tendremos acceso a la pagina.

