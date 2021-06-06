# iawpabloskiii.github.io

Para esta practica prepararemos el despliegue mediante github pages de una web personal, pero en este caso mediante el uso de mkdocs en lugar de jekyll.
La instalación se hara de manera similar, tendremos que descargar docker y docker compose y, en una maquina virtual con el repositorio de github alojado ejecutamos el siguiente comando dentro de este para descargar las dependencias necesarias

```
nuevo: docker run --rm -it -p 8000:8000 -v "$PWD":/docs squidfunk/mkdocs-material new .
```
una vez hecho esto con el siguiente comando construiremos el sitio en si, podremos añadir nuestros md en la carpeta docs
```
generar: docker run --rm -it -v "$PWD":/docs squidfunk/mkdocs-material build
```
una vez añadidos todos los ficheros que necesitemos podemos implementarlo en github con el siguiente comando
```
subir a github: docker run --rm -it -v ~/.ssh:/root/.ssh -v "$PWD":/docs squidfunk/mkdocs-material gh-deploy
```
