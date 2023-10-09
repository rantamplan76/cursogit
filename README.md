# cursogit
Proyecto de aprendizaje y recordatorio con git

# ¿Tengo git instalado?
git --version

# Configuracion inicial
-- Indicamos nuestro nombre y email para los commits
git config --global user.name "Escribe aqui tu nombre"
git config --global user.email aquivatu@correo.electronico

-- Indicamos nuestro editor
git config --global core.editor "code --wait"

-- Ver nuestra configuración global
git config --global -e

-- Añadir el caracter CR/LF en windows (true en windows / input en Mac/Linux)
git config --global core.autocrlf true/input

# Uso de GIT
-- Inicializamos el repositorio (se crea el directorio oculto .git)
git init

-- Ver estado de la carpeta
git status
-- version reducida
git status -s
-- Ver cambios pendientes de pasar a stage
git diff
-- Cambios pendientes de stage a commit
git diff --staged

-- Añadir archivos a stage (con . se añade todo | acepta expresiones regulares)
git add [archivo|carpeta|.]
-- Renombrar archivos
git mv nombreViejo nombreNuevo

-- Descartar cambios y recuperar de stage
git restore nombreDeArchivo

-- Realizar un commit (crea un commit con lo que hay en stage)
git commit -m "Descripción del commit"

-- Ver registro de commits (--oneline para version simplificada)
git log [--oneline]

-- Para ignorar archivos o rutas hay que añadirlos al archivo .gitignore

*** RAMAS ***
-- Crear una rama
git checkout -b nombreDeLaRama

-- Unir ramas. Desde la rama de destino ejecutar
git merge nombreDeLaRamaAUnir

*** GitHub ***
-- Para subir una rama nueva
git push -u origin nombreDeLaRama
-- Para subir a una rama existente
git push

-- Recuperar cambios remotos
git fetch
-- Mergear cambios remotos
git merge
-- Recuperar y mergear ennun solo comando
git pull