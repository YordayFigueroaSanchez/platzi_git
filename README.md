#
# [Configuración Inicial de Git: init y config](https://platzi.com/home/clases/11059-gitgithub/71785-configuracion-de-git-y-git-init/)
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

# [Comandos Básicos de Git: add, commit y log](https://platzi.com/home/clases/11059-gitgithub/71786-comandos-basicos-de-git-add-commit-log/)
## Para agregar un archivo al stage
git add testing.txt
## Para regresar del stage al directorio
git rm --cache testing.txt
# [Ramas y Fusión de Cambios: branch, merge, switch y checkout](https://platzi.com/home/clases/11059-gitgithub/71787-ramas-y-fusion-de-cambios-branch-merge-checkout/)
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
git revert hash_del_commit
aparece la ventana para agregar info al comentario
despues Ctrl + C, para despues : y escribir wq para escribir y salir
git reset: Este comando devuelve a un commit anterior, eliminando los cambios en el historial como si nunca hubieran ocurrido.
Permite deshacer cambios y mover el puntero HEAD a un commit específico. Hay tres modos principales:
git reset --soft: Mueve HEAD al commit especificado, pero mantiene los cambios en el área de preparación.
git reset --mixed: (Por defecto) Mueve HEAD y deshace los cambios en el área de preparación, pero mantiene los cambios en el directorio de trabajo.
git reset --hard: Mueve HEAD y descarta todos los cambios, tanto en el área de preparación como en el directorio de trabajo.
git revert: Crea un nuevo commit que deshace los cambios de un commit específico. Es útil para deshacer cambios de forma segura en repositorios compartidos.
# [Gestión de versiones: tag y checkout](https://platzi.com/home/clases/11059-gitgithub/71789-gestion-de-versiones-con-tag-y-checkout/)
## crear tag con mensaje
git tag -a v1.0 -m "Mi primer tag"
## lista los tags
git tag 
## elimina un tag
git tag -d v1.0
## 
git checkout hash_del_commit
# [Cómo Resolver Conflictos de Ramas en Git](https://platzi.com/home/clases/11059-gitgithub/71790-resolucion-de-conflictos-en-git/)
# [Clase 16 de 42 - Trabajo con repositorios remotos: push, pull y fetch](https://platzi.com/home/clases/11059-gitgithub/71797-trabajo-con-repositorios-remotos-push-pull-y-fetch/)

