# Práctica 1

## Comandos git

### git clone

Permite clonar un repositorio existente en un directorio nuevo

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas> git clone https://github.com/Pedro-Cuevas/hello-world.git p1
Cloning into 'p1'...
remote: Enumerating objects: 38, done.
remote: Counting objects: 100% (38/38), done.
remote: Compressing objects: 100% (23/23), done.
Receiving objects:  50% (19/38)sed 31 (delta 0), pack-reused 0
Receiving objects: 100% (38/38), 58.97 KiB | 1.68 MiB/s, done.
Resolving deltas: 100% (1/1), done.
```

### git status

Muestra el estado del directorio, comparando sus archivos con los de HEAD commit

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git status
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
(use "git add <file>..." to include in what will be committed)
        comandos.md

nothing added to commit but untracked files present (use "git add" to track)
```

### git add

Permite comenzar a rastrear archivos. En el ejemplo uso `git add .` El punto indica que se rastrearán todos los archivos del directorio

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git add .
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git status
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
(use "git restore --staged <file>..." to unstage)
        new file:   comandos.md
```

### git commit

Confirmamos los cambios que hemos realizado, con un mensaje. Para incluir el mensaje usamos `git commit -m "mensaje"`

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git commit -m "He añadido el archivo que explica los comandos de la práctica"
[main 3deb232] He añadido el archivo que explica los comandos de la práctica
1 file changed, 33 insertions(+)
create mode 100644 comandos.md
```

### git push

Permite subir los commits desde mi rama (branch) al repositorio remoto

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git push
info: please complete authentication in your browser...
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 895 bytes | 895.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/Pedro-Cuevas/hello-world.git
48fe276..3deb232  main -> main
```

### git checkout

git checkout permite cambiar entre ramas o restaurar los archivos del árbol de trabajo. Añadir `-b feature/1` hará que se cree una nueva rama llamada feature/1

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git checkout -b feature/1
Switched to a new branch 'feature/1'
```

En este caso cambiaríamos a la rama main usando `git checkout main`

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
```
***

## Anexo: otros comandos git

### git log

Permite ver el historial de confirmaciones

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git log
commit 8b8f03ab4f94d5e3d82e74e08e6b64f8c23cb88d (HEAD -> main, origin/main, origin/HEAD)
Author: Pedro-Cuevas <prcuevasolarte@gmail.com>
Date:   Mon Jan 24 00:11:25 2022 +0100

    estilo nuevo

commit a7af6d296f903d6bfde0dfdeef68b1fac833bbf3
Author: Pedro-Cuevas <prcuevasolarte@gmail.com>
Date:   Sun Jan 23 23:49:03 2022 +0100

    código añadido

commit 3deb2324e1c178e5596dc21441f4cf25c385eec1
Author: Pedro-Cuevas <prcuevasolarte@gmail.com>
Date:   Sun Jan 23 23:39:45 2022 +0100

    He añadido el archivo que explica los comandos de la práctica

commit 48fe2767a1dec83ae423cca0c0f8c92204ba6f65
Merge: 5038239 5b68377
Author: Juan Antonio Breña Moral <bren@juanantonio.info>
Date:   Mon Dec 20 19:26:31 2021 +0100

    Merge pull request #1 from gitt-3-pat/feature/1

    Primera iteracion

commit 5b683771defff11ef7f0086ef25c48a3cb95deed
Author: Juan Antonio Breña Moral <bren@juanantonio.info>
Date:   Mon Dec 20 19:25:31 2021 +0100

    Primera iteracion

commit 5038239e93d2da05a94667e8f9e66a16b5353076
Author: Juan Antonio Breña Moral <bren@juanantonio.info>
Date:   Mon Dec 20 19:14:40 2021 +0100

    Initial commit
```

### git pull

Permite actualizar el repositorio local

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git pull
Already up to date.
```

### git branch

Este comando permite observar qué ramas tenemos
```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git branch
* feature/1
  main
```

### git diff

Nos permite comparar ramas. Como tenemos 2 ramas, usaré `git diff main..feature/1`, que comparará los extremos de ambas ramas

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git diff main..feature/1
diff --git a/RAMA.txt b/RAMA.txt
new file mode 100644
index 0000000..d142f44
--- /dev/null
+++ b/RAMA.txt
@@ -0,0 +1 @@
+prueba
\ No newline at end of file
diff --git a/comandos.md b/comandos.md
index 1bb4944..43c24c9 100644
--- a/comandos.md
+++ b/comandos.md
@@ -1,151 +1,75 @@
 # Práctica 1

-### git clone
+## git clone

 Permite clonar un repositorio existente en un directorio nuevo

-```powershell
-PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas> git clone https://github.com/Pedro-Cuevas/hello-world.git p1
-Cloning into 'p1'...
-remote: Enumerating objects: 38, done.
-remote: Counting objects: 100% (38/38), done.
-remote: Compressing objects: 100% (23/23), done.
-Receiving objects:  50% (19/38)sed 31 (delta 0), pack-reused 0
-Receiving objects: 100% (38/38), 58.97 KiB | 1.68 MiB/s, done.
-Resolving deltas: 100% (1/1), done.
-```
+    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas> git clone https://github.com/Pedro-Cuevas/hello-world.git p1
+    Cloning into 'p1'...
+    remote: Enumerating objects: 38, done.
+    remote: Counting objects: 100% (38/38), done.
+    remote: Compressing objects: 100% (23/23), done.
+    Receiving objects:  50% (19/38)sed 31 (delta 0), pack-reused 0
+    Receiving objects: 100% (38/38), 58.97 KiB | 1.68 MiB/s, done.
+    Resolving deltas: 100% (1/1), done.

-### git status
+## git status

 Muestra el estado del directorio, comparando sus archivos con los de HEAD commit

-```powershell
-PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git status
-On branch main
:
```

### git clean

Elimina archivos sin seguimiento. `-n` muestra qué archivos se eliminarán pero no hace nada. `-f` es necesario para eliminar

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git clean -n
Would remove .comandos.md.swp
Would remove .comandos_BASE_1968.md.swp
Would remove .comandos_LOCAL_1968.md.swp
Would remove .comandos_REMOTE_1968.md.swp
Would remove RAMA.txt
Would remove comandos_BACKUP_1968.md
Would remove comandos_BASE_1968.md
Would remove comandos_LOCAL_1968.md
Would remove comandos_REMOTE_1968.md
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git clean -f
Removing .comandos.md.swp
Removing .comandos_BASE_1968.md.swp
Removing .comandos_LOCAL_1968.md.swp
Removing .comandos_REMOTE_1968.md.swp
Removing RAMA.txt
Removing comandos_BACKUP_1968.md
Removing comandos_BASE_1968.md
Removing comandos_LOCAL_1968.md
Removing comandos_REMOTE_1968.md
```

### git reset

Permite deshacer cambios para volver a HEAD commit

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git reset
Unstaged changes after reset:
M       comandos.md
```

### git revert

Permite volever a un commit anterior. Como quería deshacer un merge, tuve que usar `-m` para especificar a qué rama volver

```powershell
PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git revert 6b9f512b9f6f601e0b14d7d315bc2150a0f0e690 -m 1
[main 5c59bd1] Revert "ramas unidas"
 2 files changed, 1 insertion(+), 24 deletions(-)
 delete mode 100644 RAMA.txt
```
***

## Instalación de JDK 17, Maven e IntelliJ

```shell
C:\Users\prcue>mvn -version
Apache Maven 3.8.4 (9b656c72d54e5bacbed989b64718c159fe39b537)
Maven home: C:\apache-maven-3.8.4
Java version: 17.0.2, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-17.0.2
Default locale: es_ES, platform encoding: Cp1252
OS name: "windows 11", version: "10.0", arch: "amd64", family: "windows"

C:\Users\prcue>java -version
java version "17.0.2" 2022-01-18 LTS
Java(TM) SE Runtime Environment (build 17.0.2+8-LTS-86)
Java HotSpot(TM) 64-Bit Server VM (build 17.0.2+8-LTS-86, mixed mode, sharing)
```

![captura_IntelliJ](image.png)
