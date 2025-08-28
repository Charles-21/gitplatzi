**Primeros pasos**

Por si se te olvida algún comando

git help 

git --version

git init
Crea la rama inicial "master" por defecto.  Crea una carpeta lalamda .git que funciona como bitácora de tu desmadre

Si no te gusta que se llame master, escribe: 

git config --global init.defaultBranch main
y luego

git branch -m main

**Configuración de usuario en git**
git config --global user.name "Charles-21"
git config --global user.email "charles07@ciencias.unam.mx"

Para confirmar: 

git config --list 

**Primeros comandos**

git status
Te dirá el estado de cada archivo

git add 
Coloca archivos en el área de staging o "la limbo"

git rm --cached archivo.txt
Sacas al archivo.txt de la limbo

git commit -m "mensaje"
registra los cambios de todo lo que hayas colocado en staging

git log
Te muestra el historial de modificaciones. Hasta arriba la más reciente


**Ramas**
Las ramas sirven para trabajar aisladamente.

git branch
te dice en qué rama estás

git checkout -b rama
crea y te lleva a una nueva rama llamada rama. En ella puedes jugar todo el desmadre que quieras sin chingar a la rama main


git switch main ó git checkout main
para moverte a la rama principal

git merge
te permite fusionar la rama secundaria o individual con la rama main

git branch -D rama
te permite eliminar la rama secundaria. Es buena practica hacerlo.


**Regresar en el tiempo**
git revert crea un commit que revierte los cambios de un commit específico sin quitarlo del historial ni chingar commits de otros compañeros

git log
para copiar el identificador del commit (hash)

git revert hash hace el commit inverso y lo deja en el historial


reset al chile utilizalo con cuidado. Si llegas a utilizarlo busca la clase correspondiente

**Tag y checkout**

git tag -a v1.0 -m "primera version estable"
marca un commit con una etiqueta descriptiva en el historial.

git show
muestra los detalles de la etiqueta

git tag -d v1.0
elimina la etiqueta alv

### GITHUB

**Configuración de SSH**

¿Por qué es mejor usar SSH en lugar de HTTPS para GitHub?
Seguridad adicional: SSH permite autenticar la computadora específica que accede a los repositorios sin necesidad de ingresar una contraseña cada vez

**Generación de llave:**

sh-keygen -t ed25519 -C "tu_correo@example.com"

-t ed25519 establece el nivel de encriptación.
-C añade un comentario con tu correo, útil para identificar la llave en GitHub.

Puedes utilizar el nombre por defecto. 

Se creará un directorio llamado ".ssh" con el archivo id_ed25519.pub el cual tiene la perra lleva

**Activar el agente y añadir llave privada**


eval "$(ssh-agent -s)"
ssh-add ~.ssh/id_ed25519


Te vas a github y agregas la llave. (Copia todo lo que encuentres en el .pub

**Verificar la coneexón con github**

ssh -T git@github.com

escribe yes

y pos clonar repos ya sabes papi apoko no? :v


**Subir y jalar información**


git pull
es para jalar los cambios de la rama main en gthub. Permite actualizar el repositorio local con los cambios de la nube

git push origin main
push es para empujar :v. Permite subir cambios del repositorio local a la nube.

MUY IMPORTANTE:
No se puede hace run git push si el repositorio de github no está sincronizado con el repositorio local. 

Hay que hacer primero un git pull! Por eso a veces no te jala wey
















