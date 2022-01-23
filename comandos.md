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

Añade todos los archivos del directorio al índice