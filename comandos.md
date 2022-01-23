# Práctica 1

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

## Anexo: otros comandos

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