# Comandos de git

- git status: podemos ver el estado de los archivos (tracked o untracked)
- git add <file>: permite controlar si un nuevo archivo o sus cambios estaban o no incluido en el git
- git add .: hace que git controle los nuevos archivos o con cambios en el proyectos
- git commit -m "mensaje que yo quiera": da la orden de guardar la versión en un uevo commit con el mensaje descriptivo que se quiera poner
- git branch: me dice en que rama estoy y cuales más hay creadas en el ordenador (IMPORTANTE: cuando se crea una rama, hasta que no se sube a github no aparece!)
- git push -u <rama>: subir los cambios (commits) a la plataforma cloud (guthub) donde se guarda el proyecto para todos. El comando -u conecta a la rama que le digamos para poner solo git push a partir de ahora (sin especificar que rama es)
- git checkout -b <rama>: permite crear una rama nueva
- git checkout <rama>: permite moverse a una rama que ya exista
- git branch -d <rama>: permite borrar una rama en el terminal


# Proceso git flow (best practices)

# 1: Crear una rama
- git pull: traerte todo lo nuevo de github para estar seguro de que se trabaja sobre la versión más actualizada
- git branch -b <rama>: crear una rama nueva provisional sobre la que vayamos a trabajar para no interferir sobre la rama main o master (sobre la que corre actualmente mi programa/producto)
- git status: para ver que efectivamente has realizado cambios y no están guardados
- git add .: añadir TODOS los cambios a un "paquete" commit que se subirá conjuntamente a git
- git status: para checkear que el paquete de cambios se han guardado y están listos para subirse a git
- git commit -m "descripción": subir el paquete de cambios con un título descriptivo de qué cambios son
- git log: para ver el último commit subido

# 2: Crear la rama en github
- git push -u origin <rama>: como es la primera vez que se usa esta rama (es nueva) en github, hay que poner el -u origin para decir que se cree en el origin de github (osea en github). Ahora existen dos ramas en github

# 3: Unificar cambios en rama main (pull request en github)
- en github se selecciona el botón "Compare & pull request" eligiendo de donde se cogen los cambios y donde se meten (en el main)
- "Merge pull request" validar la unificación en la rama main
- BEST PRACTICE: eliminar la rama de la que has sacado los cambios para no acumular ramas. IMPORTANTE: aunque la borres en github no se borra en el terminal (usar: git branch -d <rama>)

# 4: reflejr cambios de github en local (terminal)
- git checkout <rama>: irse a la rama de la que queremos sus nuevos cambios en github
- git pull: traerse los cambios al terminal
- git branch -d <rama>: para borrar la rama en el terminal