# workflow-practice
> Repositorio de prácticas para el flujo de trabajo en Github. Superplus3

# Notas personales de: Jaiwer Castillo

## Comandos GIT importantes (Iteración Básica):

#### Para descargar un repositorio desde un servidor remoto. Ejemplo: Github.
```Shell
git clone + 'URL' ya sea por SSH o HTPPS del repo (Ésto para clonar). 

$ git clone git@github.com:jaiwerc/Prueba-de-fusiones.git

Otra opción sería descargar desde de la plataforma "GitHub" con download.zip
```
#### Para mostrar archivos modificados usamos:
```Shell
git status
```
#### Para agregar un nuevo archivo o uno modificado. Ejemplo:
```Shell
git add 

$ git add touch 1.txt
```
#### Para agregar varios archivos. Ejemplo:
```Shell
git add archivo.txt carpeta/otro_archivo.txt otra_carpeta/otro_archivo.txt
```
#### Para agregar todos los archivos del proyecto. Ejemplo:
```Shell
git add -A
git add --all
```
#### Permite ver la informacion de los cambios hechos. Ejemplo:
```Shell
git log

AYUDA: Hay un comando que te permite ver la información de los cambios subidos al HEAD de una forma más dinámica, esto se puede 
producir con un 'git config --global alias.+nombre que le quieras colocar al alias "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

$ git config --global alias.superlog "git log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"

Se los recomiendo, ahorra mucho tiempo 
```
#### El comando git init se utiliza para iniciar git. Crea una zona llamada staging dentro de la memoria RAM donde se irán guardando los cambios que se hagan sobre el archivo. Ejemplo:
```Shell
git init
```
#### Para iniciar GIT, entras desde la terminal a la carpeta donde esta el proyecto y lo inicias (Se inicia una sola vez). Cuando dejas un proyecto a medias y necesitas seguir trabajando en otro momento, también debes iniciar GIT de esta forma. Ejemplo:
```Shell
$ cd proyecto git 
git init
```
#### Para confirmar la instantánea preparada en el proyecto mediante un mensaje de confirmación. Ejemplo:
```Shell
git commit
```
#### Para cargar en el HEAD los cambios realizados y establecer el mensaje del commit. Ejemplo:
```ssh
git commit -m "Texto que identifique por que se hizo el commit"

$ git commit -m "Modificando archivo README.md"
```
#### Agregar y Cargar en el HEAD los cambios realizados. El parametro `-a o --all` confirma todos los archivos en el área de trabajo (esos nuevos, con modificaciones, o incluso eliminados) automáticamente. Ejemplo:
```ssh
git commit -a -m "Texto que identifique por que se hizo el commit"
git commit -a -m "Modificando archivo README.md"
```
#### Para ver conflictos (de haberlos). Ejemplo:
```ssh
git commit -a
```
#### Si te equivocaste en el nombre del commit podriamos usar este comando para reescribir el último commit con cualquier cambio que esté en el área de preparación o un nuevo mensaje (SOLO PARA EL ÜLTIMO COMMIT REALIZADO) Ejemplo:
```ssh
Nombre de commit erróneo: Vistos los comandos git 

$ git commit --amend -m "Mejorando la lista de comandos git"

Nombre de commit actualizado: Mejorando la lista de comandos git 
```

--------------------------------------------

## Estructura de los Mensajes en los COMMITS

Al crear un commit luego de añadir los archivos modificados/creados
y estas por agregar informacion sobre lo que hiciste, lo mas práctico
es escribir unas pocas palabras para informar sobre el cambio.
Ej.
```Shell
git commit -am "Agregue la funcion eliminar"
```
Pero, en proyectos mas grandes y complejos, es mejor utilizar los
estandares propuestos. Ej.
```Shell
git commit
```
Ustedes dirán  "y donde está el mensaje?". Pués al ejecutar el commit
de esa manera, sin parametros ni nada, les abrirá un editor donde
colocar una descripcion mas amplia de lo que hicieron. La siguiente
documentacion explica la forma de escribir la informacion del commit
de una forma más detallada y explicita:

- El mensaje de un commit consiste en 3 diferentes partes
separadas por una linea en blanco: el titulo, un cuerpo
opcional y un pie opcional. Algo como lo siguiente:

-------------

type: subject

body

footer

-------------

El titulo consiste en el tipo y asunto del mensaje.
Type / Tipo

El asunto no debe contener mas de 50 caracteres,
debe iniciar con una letra mayuscula y no terminar con un punto.
El tipo es contenido en el titulo y puede ser de alguno de los siguientes casos:

- feat: Una nueva caracteristica
- fix: Se soluciono un bug
- docs: Se realizaron cambios en la documentacion
- style: Se aplico formato, comas y puntos faltantes, etc; Sin cambios en el codigo
- refactor: Refactorizacion del codigo en produccion
- perf: Un cambio en el código que mejora el desempeño
- test: Se añadieron pruebas, refactorizacion de pruebas; Sin cambios en el codigo
- chore: Actualizacion de tareas de build, configuracion del admin. de paquetes; sin cambios en el codigo

Al escribir el cuerpo (Body), requerimos de una linea en blanco
entre el titulo y el cuerpo, ademas debemos limitar la longitud
de cada linea a no mas de 72 caracteres.

El pie es opcional al igual que el cuerpo, pero este es usado
para el seguimiento de los IDs con incidencias. Ej:

Resolve: #6113
Closes: #456, #789, #45

Plantilla ejemplo:

--------------------------------------------------------

feat: Ultima documentacion del Readme

Se agregaron comandos para solucionar conflictos <br />
ademas de la informacion sobre las plantillas de <br />
los mensajes largos en los commit

Resolve: #123

--------------------------------------------------------

***[Contribucion de Jaimar Angulo](jaimarkas-readme.md)***

--------------------------------------------------------

***[Notas personales de Bresmar Bermudez](Bresmar-readme.md)***

--------------------------------------------------------

***[Notas personales de Jaiwer Castillo](Jaiwer_README.md)***
