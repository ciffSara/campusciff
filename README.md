# campusciff
Repositorio para ejercicios GIT, GITHUB, MARKDOWN

#Realizamos la configuración inicial.

soterod@SOTERODW7 MINGW64 /
$ git config --global user.name "Sara"

soterod@SOTERODW7 MINGW64 /
$ git config --global user.email saraotero@campusciff.net

#Creamos un Nuevo directorio llamado EJERCICIOS.

soterod@SOTERODW7 MINGW64 /
$ mkdir EJERCICIOS

#Nos situamos en la carpeta EJERCICIOS

soterod@SOTERODW7 MINGW64 /
$ cd EJERCICIOS

#Inicializamos el repositorio

soterod@SOTERODW7 MINGW64 /EJERCICIOS
$ git init
Initialized empty Git repository in C:/Program Files/Git/EJERCICIOS/.git/

#Creamos un Nuevo repositorio en GITHUB llamado campusciff

#
#Clonamos este nuevo repositorio en la carpeta EJERCICIOS

soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ git clone git@github.com:ciffSara/campusciff.git
Cloning into 'campusciff'...
Enter passphrase for key '/c/Users/soterod/.ssh/id_rsa':
remote: Counting objects: 3, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (3/3), done.
Checking connectivity... done.

#Comprobamos que efectivamente se ha actualizado el contenido de la carpeta
#

#Y que en el interior de la carpeta campusciff, está el fichero README.md
#

#Nos situamos en la carpeta campusciff
soterod@SOTERODW7 MINGW64 /EJERCICIOS (master)
$ cd campusciff

