# iawpabloskiii.github.io

nuevo: docker run --rm -it -p 8000:8000 -v "$PWD":/docs squidfunk/mkdocs-material new .

generar: docker run --rm -it -v "$PWD":/docs squidfunk/mkdocs-material build

subir a github: docker run --rm -it -v ~/.ssh:/root/.ssh -v "$PWD":/docs squidfunk/mkdocs-material gh-deploy
