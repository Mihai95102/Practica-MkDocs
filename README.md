# Practica-MkDocs
Práctica MkDocs

## Estructura
La estructura de directorios que usaremos será la siguiente:

<img src="./images/estructura.png" width="250"/>

## Creción de nuestro Blog:
Para crear nuestro blog ejecutaremos el siguienete comando para que se cree la estructura de MkDocs:
```bash
docker run --rm -it -p 8000:8000 -v "$PWD":/docs squidfunk/mkdocs-material new .
```

## Creación de los Posts:
Crearemos los posts en lenguaje Markdown dentro de la carpeta de "docs" y guardaremos el archivo de la siguiente forma: _practica1.md_

## Generamos el código HTML
Creados los posts con Markdown, ahora tendremos que generar el código HTML de los posts con el siguiente comando:
```bash
docker run --rm -it -v "$PWD":/docs squidfunk/mkdocs-material build
```
Cuando ejecutemos este comando se nos creará la carpeta de "site". Sacaremos todo el contenido de la carpeta dentro del directorio raíz.

## Configuración:
Para configurar la página de MkDocs, aplicando temas, título, descripción, etc. Para ello editaremos el archivo de "_mkdocs.yml_".

El archivo quedaría de la siguiente forma:
```yaml
site_name: Práctica MkDocs IAW

nav:
    - Principal: index.md
    - Acerca de: about.md
    - Práctica 1: practica1.md
    - Práctica 2: practica2.md

theme:
    name: material
    language: es
    palette:
        scheme: slate
        primary: blue
```

Una vez terminada la creación y configuración de la página, esta quedará así:

<img src="./images/pagina.png"/>