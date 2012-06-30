# Hacer historia con Git

##Temas:
1. Contar una historia
    1. git init
    2. git add
    3. git status
    4. git commit
    5. git reset
    6. git rm, git mv
    7. git stash
2. Digresiones.
    1. git branch
    2. git checkout
    3. git merge
3. Reescribir la historia.
    1. git log
    2. git rebase

## Contar una historia
* `mkdir prueba`
* `cd prueba`
* **git init**
* `vim hola.py` // print "Hola, mundo"
* **git status**
* **git add hola.py**
* `git status`
* **git commit -m "Comienza el repositorio"**
* Diagrama 1
* `vim hola.py` // Agrega punto al final
* `git status`
* `git reset --hard`
* `cat hola.py`
* Explicación hablada de `git mv` y `git rm`
* Explicación hablada de `git stash` y `git stash pop`

## Digresiones
* git branch saludar-por-nombre
* Diagrama 2
* git branch
* git checkout saludar-por-nombre
* Diagrama 3
* vim hola.py // Añadir funcionalidad de saludo por nombre
* python hola.py Jair
* git add .
* Explicación hablada de por qué git commit -a es malo.
* git commit
* git log
* Diagrama 4
* vim hola.py // Añadir funcionalidad cuando el nombre está vacío
* python hola.py
* python hola.py Jair
* Explicación de requerimiento de Alice.
* git stash
* git checkout master
* Diagrama 5
* vim hola.py // Añadir signos de exclamación
* git add .
* git commit -m "Mejora el entusiasmo del saludo."
* git checkout saludar-por-nombre
* Diagrama 6
* git log
* git stash pop
* git commit -m "Añade funcionalidad cuando el nombre está vacío."
* Diagrama 7
* git merge master
* vim hola.py // Resolver conflictos.
* git add hola.py
* git commit
* git log
* Diagrama 8
* git checkout master
* git merge saludar-por-nombre
* Diagrama 9
* git branch -d saludar-por-nombre
* Diagrama 10

## Reescribir la historia
* vim hola.py // Marco alrededor del saludo, nombre del autor.
* vim README.md // README
* git add -i y git commit
* git rebase -i
* git log
