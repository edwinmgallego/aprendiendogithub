# aprendiendogithub
aprendiendo   github

Autor: Edwin Gallego
año : 2021
mes : octubre

#documentacion de  desarrollador  Dev2.

1. Git clone
Git clone es un comando para descargarte el código fuente existente desde un repositorio remoto (como Github, por ejemplo). En otras palabras, Git clone básicamente realiza una copia idéntica de la última versión de un proyecto en un repositorio y la guarda en tu ordenador.

Hay un par de formas de descargar el código fuente, pero principalmente yo prefiero clonar de la forma con https:

git clone <https://link-con-nombre-del-repositorio>

2. Git branch
Las ramas (branch) son altamente importantes en el mundo de Git. Usando ramas, varios desarrolladores pueden trabajar en paralelo en el mismo proyecto simultáneamente. Podemos usar el comando git branch para crearlas, listarlas y eliminarlas.

Creando una nueva rama:

git branch <nombre-de-la-rama>
Este comando creará una rama en local. Para enviar (push) la nueva rama al repositorio remoto, necesitarás usar el siguiente comando:

git push <nombre-remoto> <nombre-rama>
Visualización de ramas:

git branch
git branch --list
Borrar una rama:

git branch -d <nombre-de-la-rama>
3. Git checkout
Este es también uno de los comandos más utilizados en Git. Para trabajar en una rama, primero tienes que cambiarte a ella. Usaremos git checkout principalmente para cambiarte de una rama a otra. También lo podemos usar para chequear archivos y commits.

git checkout <nombre-de-la-rama>
Hay algunos pasos que debes seguir para cambiarte exitosamente entre ramas:

Los cambios en tu rama actual tienen que ser confirmados o almacenados en el guardado rápido (stash) antes de que cambies de rama.
La rama a la que te quieras cambiar debe existir en local.
Hay también un comando de acceso directo que te permite crear y cambiarte a esa rama al mismo tiempo:

git checkout -b <nombre-de-tu-rama>
Este comando crea una nueva rama en local (-b viene de rama (branch)) y te cambia a la rama que acabas de crear.

4. Git status
El comando de git status nos da toda la información necesaria sobre la rama actual.

git status
Podemos encontrar información como:

Si la rama actual está actualizada
Si hay algo para confirmar, enviar o recibir (pull).
Si hay archivos en preparación (staged), sin preparación(unstaged) o que no están recibiendo seguimiento (untracked)
Si hay archivos creados, modificados o eliminados
5. Git add
Cuando creamos, modificamos o eliminamos un archivo, estos cambios suceden en local y no se incluirán en el siguiente commit (a menos que cambiemos la configuración).

Necesitamos usar el comando git add para incluir los cambios del o de los archivos en tu siguiente commit.

Añadir un único archivo:

git add <archivo>
Añadir todo de una vez:

git add -A
Si revisas la captura de pantalla que he dejado en la sección 4, verás que hay nombres de archivos en rojo - esto significa que los archivos sin preparación. Estos archivos no serán incluidos en tus commits hasta que no los añadas.

Para añadirlos, necesitas usar el git add:
Importante: El comando git add no cambia el repositorio y los cambios que no han sido guardados hasta que no utilicemos el comando de confirmación git commit.

6. Git commit
Este sea quizás el comando más utilizado de Git. Una vez que se llega a cierto punto en el desarrollo, queremos guardar nuestros cambios (quizás después de una tarea o asunto específico).  

Git commit es como establecer un punto de control en el proceso de desarrollo al cual puedes volver más tarde si es necesario.

También necesitamos escribir un mensaje corto para explicar qué hemos desarrollado o modificado en el código fuente.

git commit -m "mensaje de confirmación"
Importante: Git commit guarda tus cambios únicamente en local.

7. Git push
Después de haber confirmado tus cambios, el siguiente paso que quieres dar es enviar tus cambios al servidor remoto. Git push envía tus commits al repositorio remoto.

git push <nombre-remoto> <nombre-de-tu-rama>
De todas formas, si tu rama ha sido creada recientemente, puede que tengas que cargar y subir tu rama con el siguiente comando:

git push --set-upstream <nombre-remoto> <nombre-de-tu-rama>
or

git push -u origin <nombre-de-tu-rama>
Importante: Git push solamente carga los cambios que han sido confirmados.

8. Git pull
El comando git pull se utiliza para recibir actualizaciones del repositorio remoto. Este comando es una combinación del git fetch y del git merge lo cual significa que cundo usemos el git pull recogeremos actualizaciones del repositorio remoto (git fetch) e inmediatamente aplicamos estos últimos cambios en local (git merge).

git pull <nombre-remoto>
Esta operación puede generar conflictos que tengamos que resolver manualmente.

9. Git revert
A veces, necesitaremos deshacer los cambios que hemos hecho. Hay varias maneras para deshacer nuestros cambios en local y/o en remoto (dependiendo de lo que necesitemos), pero necesitaremos utilizar cuidadosamente estos comandos para evitar borrados no deseados.

Una manera segura para deshacer nuestras commits es utilizar git revert. Para ver nuestro historial de commits, primero necesitamos utilizar el  git log -- oneline:
10. Git merge
Cuando ya hayas completado el desarrollo de tu proyecto en tu rama y todo funcione correctamente, el último paso es fusionar la rama con su rama padre (dev o master). Esto se hace con el comando git merge.

Git merge básicamente integra las características de tu rama con todos los commits realizados a las ramas dev (o master).  Es importante que recuerdes que tienes que estar en esa rama específica que quieres fusionar  con tu rama de características.

Por ejemplo, cuando quieres fusionar tu rama de características en la rama dev:

Primero, debes cambiarte a la rama dev:

git checkout dev
Antes de fusionar, debes actualizar tu rama dev local:

git fetch
Por último, puedes fusionar tu rama de características en la rama dev:

git merge <nombre-de-la-rama>
Pista: Asegúrate de que tu rama dev tiene la última versión antes de fusionar otras ramas, si no, te enfrentarás a conflictos u otros problemas no deseados.

Aquí están mis 10 comandos de git más usados cuando me enfrento a la programación en mi día a día. Hay muchas más cosas que aprender sobre Git y las explicaré más adelante en oros artículos.

Si quieres aprender más sobre el desarrollo web, ¡puedes seguirme en Youtube!

¡Gracias por leerme!

tenemos  los  siguiente s   copmando aprendidos: 
 git clone:   en donde    se  clona  el repósitorio de  github
 git  fetch:   que es  donde   se  verificas  que cambios  existen  en la nube(github)
  git pull:     que es  donde se  descarga  a local
  git commit -am "donde    escribo   el  mensaje  describiendo  brevemente  el cambio realizado para  subirlo al repositorio  remoto"
  git push origin main:  es  donde  se  suben los cambios  a la  rama  principal.

