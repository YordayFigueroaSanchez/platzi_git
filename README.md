#
# [Configuracion Inicial de Git: init y config](https://platzi.com/home/clases/11059-gitgithub/71785-configuracion-de-git-y-git-init/)
git --version
git init
git config --global init.defaultBranch main
git branch -m main
git --help
git config --global user.name "yfsanchez"
git config --global user.email "yfsanchez@gmail.com"
git --list
## docs
[git-cheat-sheet-education.pdf](git-cheat-sheet-education.pdf)

# [Comandos Basicos de Git: add, commit y log](https://platzi.com/home/clases/11059-gitgithub/71786-comandos-basicos-de-git-add-commit-log/)
## Para agregar un archivo al stage
git add testing.txt
## Para regresar del stage al directorio
git rm --cache testing.txt
# [Ramas y Fusion de Cambios: branch, merge, switch y checkout](https://platzi.com/home/clases/11059-gitgithub/71787-ramas-y-fusion-de-cambios-branch-merge-checkout/)
## Crear una rama y pasar a ella
git switch -c nombre_de_la_rama
### Para hacer un merge
Estando en la rama main
git merge nombre
### Buena practica borrar ramas que no se usan
git branch -D nombre
# [Volviendo en el Tiempo en Git: reset y revert](https://platzi.com/home/clases/11059-gitgithub/71788-volviendo-en-el-tiempo-en-git-reset-revert/)
## reset
git reset hash_del_commit
tiene los parametos --hard, --soft y --mixed
## revert
`git revert hash_del_commit`
aparece la ventana para agregar info al comentario
despues Ctrl + C, para despues : y escribir wq para escribir y salir
## Este comando devuelve a un commit anterior, eliminando los cambios en el historial como si nunca hubieran ocurrido.
```
git reset
```
Permite deshacer cambios y mover el puntero HEAD a un commit especifico. Hay tres modos principales:
## Mueve HEAD al commit especificado, pero mantiene los cambios en el area de preparacion.
```
git reset --soft
```
## (Por defecto) Mueve HEAD y deshace los cambios en el area de preparacion, pero mantiene los cambios en el directorio de trabajo.
```
git reset --mixed 
```
## Mueve HEAD y descarta todos los cambios, tanto en el area de preparacion como en el directorio de trabajo.
```
git reset --hard
```
## Crea un nuevo commit que deshace los cambios de un commit especifico. Es util para deshacer cambios de forma segura en repositorios compartidos.
```
git revert
```

# [Gestion de versiones: tag y checkout](https://platzi.com/home/clases/11059-gitgithub/71789-gestion-de-versiones-con-tag-y-checkout/)
## crear tag con mensaje
```
git tag -a v1.0 -m "Mi primer tag"
```
## lista los tags
```
git tag 
```
## elimina un tag
```
git tag -d v1.0
```
## 
```
git checkout hash_del_commit
```
# [Como Resolver Conflictos de Ramas en Git](https://platzi.com/home/clases/11059-gitgithub/71790-resolucion-de-conflictos-en-git/)
## Subir los cambios
```
git push -u origin main
```
Cuando ya este creada la rama se pude lanzar 
```
git push
```
## Traer cambios y mezclarlos
```
git pull
```
## Traer cambios sin mezclarlos
```
git fetch
```
Mi test para subir a github
# [Clase 14 de 42 - Como configurar SSH para GitHub: Guia paso a paso](https://platzi.com/home/clases/11059-gitgithub/71823-configuracion-de-llaves-ssh/)
## mas robusta
ssh-keygen -t ed25519 -C "email@dominio.com"
```
ssh-keygen -t ed25519 -C "yfsanchez@gmail.com"
```
## otra
```
ssh-keygen -t rsa -b 4096 -C "email@dominio.com"
```
## agente de ssh
```
eval "$(ssh-agent -s)"
```
## agregar key
```
ssh-add ~/.ssh/id_ed25519
```
agregar la key .pub en git
## autenticar con github.com
```
ssh -T git@github.com
```

# [Clase 15 de 42 - Clone, fork y estrellas a repositorios](https://platzi.com/home/clases/11059-gitgithub/71796-clone-fork-y-estrellas-a-repositorios/)
```
git clone
```

# [Clase 16 de 42 - Trabajo con repositorios remotos: push, pull y fetch](https://platzi.com/home/clases/11059-gitgithub/71797-trabajo-con-repositorios-remotos-push-pull-y-fetch/)
Cuando el brancho no esta en git aun
```
git push -u origin main
```
Cuando ya esta el branch en git
```
git pull
```
## comprobar cambio antes de mezclarlos
Traer los cambios
```
git fetch origin
```
Comparar los cambios
```
git log main..origin/main
```
Agregar los cambios
```
git merge origin/main
```

# [Clase 17 de 42 - Gestión de Issues y Discussions en GitHub](https://platzi.com/home/clases/11059-gitgithub/71795-gestion-de-issues-y-discussions-en-github/)

# [Clase 18 de 42 - Colaboración sin errores: Pull Requests en GitHub](https://platzi.com/home/clases/11059-gitgithub/71798-colaboracion-con-pull-requests/)
## Visualizar los nuevos branch
```
git fetch origin
```
## switch al branch
```
git checkout 1-bug---agrega-algo
```