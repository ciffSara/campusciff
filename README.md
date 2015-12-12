# Campusciff
Repositorio para ejercicios GIT, GITHUB, MARKDOWN

#Realizamos la configuración inicial.
```sh
soterod@SOTERODW7 MINGW64 /
$ git config --global user.name "Sara"

soterod@SOTERODW7 MINGW64 /
$ git config --global user.email saraotero@campusciff.net
```
#Creamos un Nuevo directorio llamado EJERCICIOS:

```sh
soterod@SOTERODW7 MINGW64 /
$ mkdir EJERCICIOS
```
Nos situamos en la carpeta EJERCICIOS
```sh
soterod@SOTERODW7 MINGW64 /
$ cd EJERCICIOS
```
Inicializamos el repositorio
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS# (GitHub-Flavored) Markdown Editor

Basic useful feature list:

 * Ctrl+S / Cmd+S to save the file
 * Ctrl+Shift+S / Cmd+Shift+S to choose to save as Markdown or HTML
 * Drag and drop a file into here to load it
 * File contents are saved in the URL so you can share files


I'm no good at writing sample / filler text, so go write something yourself.

Look, a list!

 * foo
 * bar
 * baz

And here's some code! :+1:

```javascript
$(function(){
  $('div').html('I am a div.');
});
```

This is [on GitHub](https://github.com/jbt/markdown-editor) so let me know if I've b0rked it somewhere.


Props to Mr. Doob and his [code editor](http://mrdoob.com/projects/code-editor/), from which
the inspiration to this, and some handy implementation hints, came.

### Stuff used to make this:

 * [markdown-it](https://github.com/markdown-it/markdown-it) for Markdown parsing
 * [CodeMirror](http://codemirror.net/) for the awesome syntax-highlighted editor
 * [highlight.js](http://softwaremaniacs.org/soft/highlight/en/) for syntax highlighting in output code blocks
 * [js-deflate](https://github.com/dankogai/js-deflate) for gzipping of data to make it fit in URLs

$ git init
Initialized empty Git repository in C:/Program Files/Git/EJERCICIOS/.git/
```

#2.1 REPOSITORIO CAMPUSCIFF

**1 Creamos un Nuevo repositorio en GITHUB llamado campusciff**

![Repositorio](/img/repositorio.jpg)

**2 Clonamos este nuevo repositorio en la carpeta EJERCICIOS**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git clone git@github.com:ciffSara/campusciff.git
Cloning into 'campusciff'...
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.
```
Comprobamos que efectivamente se ha actualizado el contenido de la carpeta

![Carpeta](/img/carpeta.jpg)

#2.2 README

Y que en el interior de la carpeta campusciff, está el fichero README.md

![interior de la carpeta](/img/intCarpeta.jpg)

#2.3 COMMIT Y PUSH INICIAL

Nos situamos en la carpeta campusciff.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff
```
Subimos el fichero al Staging area.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git add README.md
```
Subimos el fichero al repositorio local.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git commit -m "Commit inicial"
[master a464442] Commit inicial
 1 file changed, 50 insertions(+)
```
Subimos el fichero al repositorio remoto.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git push origin master
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 846 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:ciffSara/campusciff.git
   41483ed..a464442  master -> master
```
#2.4 IGNORAR ARCHIVOS

Creamos en local un fichero privado.txt
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ echo privado>privado.txt
```
Creamos una carpeta con el nombre de privada.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ mkdir privada
```
Comprobamos que se han creado correctamente
![Carpeta privada](/img/privada.jpg)

Creamos un fichero .gitignore con el nombre de los ficheros/carpetas que 
queremos que git ignore.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ echo privada > .gitignore
```
Añadimos el nombre del fichero.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ echo privado.txt >> .gitignore
```
Comprobamos el contenido del fichero .gitignore
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ cat .gitignore
privada
privado.txt
```
Subimos este nuevo fichero al repositorio local
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git add .gitignore
warning: LF will be replaced by CRLF in .gitignore.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git commit -m "Añadimos .gitignore"
[master 47690f8] Añadimos .gitignore
warning: LF will be replaced by CRLF in .gitignore.
The file will have its original line endings in your working directory.
 1 file changed, 2 insertions(+)
 create mode 100644 .gitignore
```
Para comprobar que GIT ha ignorado los archivos indicados subimos al repositorio remoto.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git push origin master
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 304 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:ciffSara/campusciff.git
   a464442..47690f8  master -> master
```
Y observamos que únicamente se ha subido el fichero .gitignore

![Ficheros privados](/img/gitignore1.jpg)

Comprobamos también el contenido del fichero .gitignore

![Fichero gitignore](/img/gitignore2.jpg)

Donde aparecen los nombres de los archivos a ignorar.

#2.5 CREAR EL TAG V0.1

**1 Creamos un fichero, 1.txt**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ echo 1 > 1.txt
```
Subimos ese nuevo fichero al repositorio local
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git add 1.txt
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git commit -m "Añadimos fichero 1.txt"
[master 43b6a6d] Añadimos fichero 1.txt
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
 1 file changed, 1 insertion(+)
 create mode 100644 1.txt
```
**2 Creamos una etiqueta**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git tag "v0.1"
```
Comprobamos que se ha creado la etiqueta.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git tag
v0.1

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git show v0.1
commit 43b6a6d7635cc4d02632d858d26ed7153256d854
Author: Sara <saraotero@campusciff.net>
Date:   Mon Nov 30 18:40:31 2015 +0100

    Añadimos fichero 1.txt

diff --git a/1.txt b/1.txt
new file mode 100644
index 0000000..d00491f
--- /dev/null
+++ b/1.txt
@@ -0,0 +1 @@
+1
```
**3 Subimos los cambios al repositorio remoto**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git push origin master
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 320 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:ciffSara/campusciff.git
   47690f8..43b6a6d  master -> master
```
![Fichero 1](/img/1.jpg)

#2.6 CREAR UNA RAMA REMOTA V0.2

**1 Creamos una nueva rama v0.2**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git branch v0.2
```
**2 posicionamos la carpeta de trabajo en dicha rama.**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git checkout v0.2
Switched to branch 'v0.2'

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$
```
Subimos la rama al repositorio remoto
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git push origin v0.2
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Total 0 (delta 0), reused 0 (delta 0)
To git@github.com:ciffSara/campusciff.git
 * [new branch]      v0.2 -> v0.2
```
![Rama](/img/rama v02.jpg)

**3 Añadimos el nuevo fichero 2.txt a la rama v0.2**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ echo 2 > 2.txt
```
**4 Y lo subimos al repositorio remoto**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git add 2.txt
warning: LF will be replaced by CRLF in 2.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git commit -m "Subimos el fichero 2.txt a la rama v0.2"
[v0.2 ccc9617] Subimos el fichero 2.txt a la rama v0.2
warning: LF will be replaced by CRLF in 2.txt.
The file will have its original line endings in your working directory.
 1 file changed, 1 insertion(+)
 create mode 100644 2.txt

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git push origin v0.2
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 354 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:ciffSara/campusciff.git
   43b6a6d..ccc9617  v0.2 -> v0.2
```
![Comprobamos en GITHUB el contenido de la nueva rama](/img/rama v2.jpg)

#2.7 MERGE DIRECTO

**1 Nos volvemos a posicionar en la rama master**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$
```
**2 Hacemos un merge de la rama v0.2**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git merge v0.2
Updating 43b6a6d..ccc9617
Fast-forward
 2.txt | 1 +
 1 file changed, 1 insertion(+)
 create mode 100644 2.txt
```
Merge sin conflictos.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git list
* ccc9617 (HEAD -> master, origin/v0.2, v0.2) Subimos el fichero 2.txt a la rama v0.2
* 43b6a6d (tag: v0.1, origin/master, origin/HEAD) Añadimos fichero 1.txt
* 47690f8 Añadimos .gitignore
* a464442 Commit inicial
* 41483ed Initial commit
```
![Comprobamos el contenido de la rama master en GitHub](/img/merge sin conflictos.jpg)

Dónde ahora aparece también el fichero 2.txt

#2.8 MERGE CON CONFLICTO

**1 Añadimos la palabra Hola al fichero 1.txt de la rama master**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ echo Hola >> 1.txt

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ cat 1.txt
1
Hola
```
Subimos los cambios al repositorio local
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git add .
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git commit -m "Modificación del fichero 1.txt en la rama master"
[master warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
4a911f1] Modificación del fichero 1.txt en la rama master
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
 1 files changed, 1 insertions(+)
 ```
**2 Cambiamos a la rama v0.2**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git checkout v0.2
Switched to branch 'v0.2'

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$
```
Comprobamos el contenido del fichero 1.txt
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ cat 1.txt
1
```
Añadimos la palabra Adios al fichero
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ echo Adios >> 1.txt
```
Comprobamos que se ha añadido el nuevo texto
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ cat 1.txt
1
Adios
```
Subimos los cambios al repositorio local
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git add .
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git commit -m "Modificación del fichero 1.txt en la rama v0.2"
[v0.2 warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
b0e932b] Modificación del fichero 1.txt en la rama v0.2
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
 1 file changed, 1 insertion(+)
```
**3 Nos volvemos a posicionar en la rama master**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git checkout master
Switched to branch 'master'
Your branch is up-to-date with 'origin/master'.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$
```
Y hacemos un merge con la rama v0.2
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git merge v0.2
Auto-merging 1.txt
CONFLICT (content): Merge conflict in 1.txt
Automatic merge failed; fix conflicts and then commit the result.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$
```
Se ha producido un conflicto ya que el fichero 1.txt contiene distinta información en ambas ramas.
```sh
1
<<<<<<< HEAD
Hola
=======
Adios
>>>>>>> v0.2
```
**4 Listamos las ramas con merge y sin**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$ git branch --merged
* master

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$ git branch --no-merged
  v0.2
```
**5 Solucionamos el conflicto modificando los archivos 1.txt de ambas ramas.**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$ echo Adios>1.txt

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ cat 1.txt
Adios

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$ git add .
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master|MERGING)
$ git commit -m "Modificamos 1.txt para solucionar conflictos rama master"
[master 5e034f2] Modificamos 1.txt para solucionar conflictos rama master
```
Y la rama v0.2
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git checkout v0.2
Switched to branch 'v0.2'

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ echo Adios>1.txt

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git add .
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ git commit -m "Modificamos 1.txt para solucionar conflictos rama v0.2"
[v0.2 warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
8a1c872] Modificamos 1.txt para solucionar conflictos rama v0.2
warning: LF will be replaced by CRLF in 1.txt.
The file will have its original line endings in your working directory.
 1 file changed, 1 deletion(-)

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (v0.2)
$ cat 1.txt
Adios
```sh
Volvemos a hacer el merge
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git merge v0.2 -m "Merge tras arreglar los conflictos"
Already up-to-date.
```
Y ahora indica que los fichero son iguales, tal y como esperábamos.

#2.9 BORRAR RAMA

**1 Creamos una nueva etiqueta v0.2**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git tag v0.2

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git tag
v0.1
v0.2
```
**2 Listamos los commits, las ramas y las etiquetas realizadas.**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git list
*   89f6b8c (HEAD -> master, tag: v0.2) Merge branch 'v0.2'
|\
| * 8a1c872 (v0.2) Modificamos 1.txt para solucionar conflictos rama v0.2
* |   5e034f2 Modificamos 1.txt para solucionar conflictos rama master
|\ \
| |/
| * b0e932b Modificación del fichero 1.txt en la rama v0.2
* | 5cb2b2b (origin/master, origin/HEAD) Delete ~WRL3220.tmp
* | 52ab69f Modificación del fichero 1.txt en la rama master
* | 4a911f1 Modificación del fichero 1.txt en la rama master
|/
* ccc9617 (origin/v0.2) Subimos el fichero 2.txt a la rama v0.2
* 43b6a6d (tag: v0.1) Añadimos fichero 1.txt
* 47690f8 Añadimos .gitignore
* a464442 Commit inicial
* 41483ed Initial commit
```
**3 Borramos la rama v0.2 del repositorio local**
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git branch -d v0.2
Deleted branch v0.2 (was 8a1c872).
```
Comprobamos que ya sólo aparece la rama master.
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git branch
* master

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff (master)
$ git branch -v
* master 89f6b8c [ahead 4] Merge branch 'v0.2'
```
#2.10 CUENTA DE GITHUB

**1 Añadir foto al perfil de GitHub**

![Foto perfil](/img/foto perfil.jpg)

**2 Poner doble factor de autentificación**

![Two-Factor authentication](/img/autentificacion.jpg)

**3 Comprobar que tenemos la clave pública en el ordenador**

![SSH Keys](/img/SSH Key.jpg)

#2.11 USO SOCIAL DE GITHUB

**1 Seguir a los compañeros de clase**

![Compañeros de clase](/img/following.jpg)

**2 Seguir los repositorios campusciff de los compañeros**

![Repositorios campusciff](/img/watch.jpg)

**3 Añadir estrellas a los repositorios campusciff de los compañeros.**

![Estrellas](/img/estrellas.jpg)

#2.12 CREAR UNA TABLA

**1 Crear una tabla con el nombre y el enlace a github de varios compañeros**

NOMBRE | GITHUB 
-------|-------
César Hernández| https://github.com/ciffcesarhernandez
José Dios |https://github.com/jrdios
asuarezg|https://github.com/asuarezg

#2.13 COLABORADORES
Añadir colaboradores

![Añadir colaborador](/img/colaborador.jpg)

#2.14 CREAR UNA ORGANIZACIÓN

![Crear una organización](/img/organizacion.jpg)

#2.15 CREAR EQUIPOS

**1 Crear dos equipos en la organización**

Crear un equipo de administradores y otro de colaboradores, este último con menos permisos:

![Equipo de administradores y equipo de colaboradores](/img/equipos.jpg)

**2 Invitamos a 3 personas al equipo de administradores**

![Administradores](/img/admin.jpg)

**3 Invitamos a 3 personas al equipo de colaboradores**

![Colaboradores](/img/colaboradores.jpg)

#2.16 CREAR UN INDEX.HTML

**1 Crear un index.html**

Creamos un archivo html y lo subimos al repositorio
```sh
soterod@SOTERODW7 MINGW64 /
$ cd EJERCICIOS

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git init
Reinitialized existing Git repository in C:/Program Files/Git/EJERCICIOS/.git/

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git clone git@github.com:campusciff-ciffSara/campusciff-ciffSara.github.io.git
Cloning into 'campusciff-ciffSara.github.io'...
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
warning: You appear to have cloned an empty repository.
Checking connectivity... done.

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff-ciffSara.github.io

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-ciffSara.github.io (master)
$ git add index.html

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-ciffSara.github.io (master)
$ git commit -m "Commit de index"
[master (root-commit) eb1a309] Commit de index
 1 file changed, 9 insertions(+)
 create mode 100644 index.html

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-ciffSara.github.io (master)
$ git push origin master
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 312 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:campusciff-ciffSara/campusciff-ciffSara.github.io.git
 * [new branch]      master -> master
```
Comprobamos que se ha subido

![Archivo index](/img/index.jpg)

###Link a la página wed de la organización

[Página web de la organización](https://campusciff-ciffsara.github.io)

#2.17 CREAR PULL-REQUESTS

**1 Hacer dos forks**

Fork 1
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-ciffSara.github.io (master)
$ cd -
/EJERCICIOS

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git clone git@github.com:campusciff-ciffSara/campusciff-Miriam-Asenjo.github.io.git
Cloning into 'campusciff-Miriam-Asenjo.github.io'...
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
remote: Counting objects: 9, done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 9 (delta 1), reused 9 (delta 1), pack-reused 0
Receiving objects: 100% (9/9), done.
Resolving deltas: 100% (1/1), done.
Checking connectivity... done.
```
Fork 2
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git clone git@github.com:campusciff-ciffSara/campusciff-macarenagaranena.github.io.git
Cloning into 'campusciff-macarenagaranena.github.io'...
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
remote: Counting objects: 10, done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 10 (delta 0), reused 10 (delta 0), pack-reused 0
Receiving objects: 100% (10/10), done.
Checking connectivity... done.

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff-macarenagaranena.github.io
```

**2 Creamos una rama en cada fork**

Fork 1
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff-Miriam-Asenjo.github.io

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-Miriam-Asenjo.github.io (master)
$ git checkout -b ramaSara
Switched to a new branch 'ramaSara'

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-Miriam-Asenjo.github.io (ramaSara)
```
Fork 2
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-macarenagaranena.github.io (ramaSara)
$ cd -
/EJERCICIOS
```
**3 Modificamos el fichero index**

Fork 1
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff-Miriam-Asenjo.github.io

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-Miriam-Asenjo.github.io (ramaSara)
$ git add index.html

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-Miriam-Asenjo.github.io (ramaSara)
$ git commit -m "modificación index fork"
[ramaSara 29672e0] modificación index fork
 1 file changed, 1 insertion(+)

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-Miriam-Asenjo.github.io (ramaSara)
$ git push origin ramaSara
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 375 bytes | 0 bytes/s, done.
Total 3 (delta 1), reused 0 (delta 0)
To git@github.com:campusciff-ciffSara/campusciff-Miriam-Asenjo.github.io.git
 * [new branch]      ramaSara -> ramaSara
```

![Index modificado](/img/index1.jpg)

Fork 2
```sh
soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-macarenagaranena.github.io (ramaSara)
$ git add index.html

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-macarenagaranena.github.io (ramaSara)
$ git commit -m "Modificación index fork"
[ramaSara f46fe27] Modificación index fork
 1 file changed, 2 insertions(+)

soterod@SOTERODW7 MINGW64 /EJERCICIOS/campusciff-macarenagaranena.github.io (ramaSara)
$ git push origin ramaSara
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
Counting objects: 3, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 385 bytes | 0 bytes/s, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:campusciff-ciffSara/campusciff-macarenagaranena.github.io.git
 * [new branch]      ramaSara -> ramaSara
 ```
 
![Index modificado](/img/index2.jpg)

**4 Hacer pull request **

Pull request del primer folk:

![Pull Request del primer folk](/img/pullRequest2.jpg)

Pull request del segundo folk:

![Pull Request del segundo folk](/img/pullRequest1.jpg)

#2.18 GESTIONAR PULL-REQUESTS

Aceptar los pull-request que lleguen a los
repositorios de tu organización.