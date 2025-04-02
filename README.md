# GitHubEssential

- Comandos Esenciales de GitHub para el uso cotidiano.

## Introducción

En este documento revisaremos de forma rápida y sencilla los comandos más utilizados de **Git** y **GitHub**. Tanto de una rama local como en GitHub.

## Comandos de Git

### Para repositorio local :computer:

### Si es la primera vez que utilizamos el repositorio :arrow_down:

1. **git clone**    : Será el primer llamado que realicemos para copiar de un repositorio remoto a nuestro entorno local. Siendo las opciones disponibles ***HTTPS, SSH, CLI***
***Es importante tener claro en que rama vamos a trabajar y no modificar directamente main.***
2. **git branch**   : De esta forma la consola nos indicará en que rama estamos ubicados mediante un '*'.
3. **git checkout -b 'BRANCH_NAME'** : Para crear una nueva rama utilizaremos este comando. De forma automática nos ubicará a esta nueva rama.
4. **git switch 'BRANCH_NAME'** : En caso de no estar en la rama correcta con este comando podemos desplazarnos a la correcta.
5. **git status**   : Con este comando podemos ver los cambios y el estado de nuestro repositorio local.
6. **git add .**    : Una vez revisados los cambios y estando seguros que podemos avanzar, utilizamos este comando para mover a *Stage* las modificaciones realizadas.
7. **git commit -m "*MESSAGE*"** : Commit se encarga de realizar un comentario sobre los cambios añadidos recientemente y tenerlos listos para subir a cloud.
8. **git push -u origin 'BRANCH'**     : Realizado el comentario de nuestro cambios podemos realizar la carga al repositorio en cloud para ser recibido por ***PULL REQUEST*** y realizar ***code review***

### PULL REQUEST

- Desde esta sección veremos los cambios realizados por cada usuario mediante **git push -u origin 'BRANCH'** desde su respectivo repositorio local intentando agregarlos al contenido de main.

- Asignaremos el título y descripción del cambio realizados y avanzaremos a crear el pull request.

- De manera automática git revisará que no haya ramas en conflicto y permitirá que sea revisada por otro usuario.

- Esta sección debe ser estrictamente revisada y aprobada por el resto de miembros para indicar si hay un error o modificación necesaria antes de agregarlo al código principal.

- De estar correcto es aprobado utilizando ***Merge pull request.*** y la rama se fusiona con la rama principal luego procederemos a eliminar la rama en la que trabajamos mediante ***Delete banch.***

### Nuevamente trabajando en local

1. **git pull** : El primer comando que debemos realizar es actualizar nuestro repositorio local al repositorio cloud. De esta manera no tendremos entrelazamiento de ramas por elementos desactualizados al momento de fusionar ramas (no es infalible).
2. De aquí en adelante podemos seguir el resto de pasos al igual que la primera vez.

### Comandos de consulta

- **git status** : Consutar estado de archivos y carpetas en nuestro entorno local.
- **git log**    : Consultar el historial de commits realizados.
- **git branch** : Consultar la rama en la que estamos ubicados.

### Ramas-Branch

::: mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
:::