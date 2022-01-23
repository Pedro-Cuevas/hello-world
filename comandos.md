# Práctica 1

## git clone

Permite clonar un repositorio existente en un directorio nuevo

    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas> git clone https://github.com/Pedro-Cuevas/hello-world.git p1
    Cloning into 'p1'...
    remote: Enumerating objects: 38, done.
    remote: Counting objects: 100% (38/38), done.
    remote: Compressing objects: 100% (23/23), done.
    Receiving objects:  50% (19/38)sed 31 (delta 0), pack-reused 0
    Receiving objects: 100% (38/38), 58.97 KiB | 1.68 MiB/s, done.
    Resolving deltas: 100% (1/1), done.

## git status

Muestra el estado del directorio, comparando sus archivos con los de HEAD commit

    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Untracked files:
    (use "git add <file>..." to include in what will be committed)
            comandos.md

    nothing added to commit but untracked files present (use "git add" to track)


## git add .

Permite comenzar a rastrear archivos. El punto indica que se rastrearán todos los archivos del directorio

    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git add .
    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git status
    On branch main
    Your branch is up to date with 'origin/main'.

    Changes to be committed:
    (use "git restore --staged <file>..." to unstage)
            new file:   comandos.md

## git commit -m "tu mensaje"

Confirmamos los cambios que hemos realizado, con un mensaje.

    PS C:\Users\prcue\OneDrive\Estudios\curso 3\Programación de Aplicaciones Telemáticas\p1> git commit -m "He añadido el archivo que explica los comandos de la práctica"
    [main 3deb232] He añadido el archivo que explica los comandos de la práctica
    1 file changed, 33 insertions(+)
    create mode 100644 comandos.md

## git push

Permite subir los commits desde mi rama (branch) al repositorio remoto

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