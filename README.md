# PPS-Unidad0Actividad4-Angel

Vamos a hacer una nueva actividad con git. En esta ocasión crearemos un pequeño proyecto de una página web que podremos visualizar creando un pequeño servidor con php. Como en la actividad anterior el producto a realizar será el repositorio en github. Allí tendrás que documentar la realización de la práctica con la explicación del procedimiento, sus imágenes, etc.


## Configuración de Git

1. Configurar el editor de comandos, para ello ejecutamos `git config --global core.editor nano`

![](Images/img1.png)

2. Configurar git para que al utilizar `git dif` o `git log` se muestre el mensaje completo sin entrar en el editor, ejecutamos `git config — global core.pager ' ' `

![](Images/img2.png)

3. Ajustamos los valores de las variables de Git, para ello ejecutamos

* git config  — global color.status auto
* git config  — global color.branch auto
* git config  — global color.interactive auto
* git config  — global color.diff auto

![](Images/img3.png))

## Creación de Proyecto y repositorio

Creamos un nuevo repositorio con el siguiente nombre: PPS-Unidad0Actividad4-TuNombre

## Iniciando Proyecto

1. Haz un listado en forma de arbol (`tree -a`) de todos los archivos del directorio.

![](Images/img4.png)

2. Crea un archivo con nombre README (si no existe todavía) y lo añades al proyecto.
3. Comprueba el estado de git (`git status -s` o `git status --short`.

![](Images/img5.png)

4. Escribe en él una descripción de la actividad y vuelves a comprobar su estado.

## Ignorando archivos

1. Crea una carpeta con nombre Excluded. En ella vamos a colocar la documentación que no queremos que sea rastreada y subida al repositorio.

2. Para comprobar que funciona crea algún archivo vacío allí y también crea un archivo con nombre excluido.txt en el directorio principal del repositorio.

![](Images/img6.png)
![](Images/img7.png)

3. Crea un archivo con nombre .gitignore en el cual vamos a poner los archivos y directorios que no queremos que se rastreen.

![](Images/img8.png)

4. Indica en el .gitignore que los archivos con extensión .txt y el directorio Excluded no deben de ser rastreados ni sincronizados.

![](Images/img9.png)

5. Comprueba el estado del proyecto y comprueba que no nos indica nada del seguimiento de dichos archivos.

![](Images/img10.png)


## Trabajo con Git

1. Crea un archivo con nombre index.html.

2. Introduce el código html para que nos muestre un mensaje de Hola mundo con tu nombre. Uno sencillo sería este:

```html
   <H1>Hola $USER¡¡¡ ¿Qué tal te encuentras?</H1>
```

![](Images/img11.png)

3. Visualiza el estado del proyecto ( puedes hacer tambien un git status corto `git status --s` o `git status --short`).

![](Images/img12.png)

4. Puedes ver como te indica que tienes varias operaciones por hacer: git add, git commit...


5. Añade el archivo index.html al proyecto (git add).


6. Haz un commit (Puedes hacer ``commit -am "commentario del commit"` de esta manera se añaden las modificaciones de archivos y se hace el commit con el mensaje indicado sin abrir el archivo y tener que escribir nosotros).

7. Vuelve a comprobar el estado del proyecto. Puedes ver como ya debería de estar todo en orden.

8. Vuelve a subir los cambios a tu repositorio de github (git push)

![](Images/img13.png)

## Creación de nuestro servidor web y visualización de nuestro proyecto

1. En un nueva pestaña de terminal y en el mismo directorio, ejecuta `php -S 0:8080` para lanzar un servidor con la página html que has creado.

![](Images/img14.png)

2. Visualiza la página creada, puedes acceder a ella en tu navegador en el puerto 8080 de tu equipo, es decir, 127.0.0.1:8080

![](Images/img15.png)

## Seguimos Trabajando con Git

1. Haz una copia del archivo local index.html con el nombre index.html.save. Modifica el fichero index.html para que cambie el texto mostrado en la página web.

![](Images/img16.png)
![](Images/img18.png)
![](Images/img19.png)

2. Verifica estado del proyecto.

![](Images/img17.png)

3. Comprueba las diferencias de los archivos que no han sido añadidos (`git diff`)

![](Images/img20.png)

4. Refresca navegador para comprobar que ha cambiado el contenido de nuestra página web.

![](Images/img21.png)

5. Vuelve a la versión anterior del archivo index.html (`git restore`).

![](Images/img22.png)

6. Vuelve a refrescar navegador para ver como vuelve a versión inicial.

![](Images/img23.png)

7. Utiliza el comando `git mv` para sobreescribir el archivo index.html con index.html.save

![](Images/img27.png)

8. Mira el estado del proyecto y confirma todos los cambios.

![](Images/img26.png)

9. Para pull y push, haz un push y comprueba cómo han subido los archivos a github.com.

![](Images/img28.png)

10. Modifica el archivo index.php desde la página de github.com y haz un pull y comprueba cómo se ha modificado la página web en nuestro navegador.

![](Images/img29.png)

![](Images/img30.png)

## Git log

1. En la siguiente página podemos encontrar información sobre los comandos de git log [Git Book sobre los comandos git log](https://git-scm.com/book/es/v2/Fundamentos-de-Git-Ver-el-Historial-de-Confirmaciones)

2. Muestra los logs

![](Images/img31.png)

3. Muestra los logs de los últimos 3 commits

![](Images/img32.png)

4. Muestra los logs utilizando el modificador ``--pretty`

![](Images/img33.png)

5. Muestra los logs de los últimos 2 commits donde se vean las diferencias de cada una de las entradas.

![](Images/img34.png)

6. Muestra los logs de las modificaciones realizadas en el último día

![](Images/img35.png)

## Ramas

1. Lista las ramas existentes.

Para listar las ramas locales usamos `git branch` y para las remotas `git branch -a`. 

![](Images/img36.png)

2. Crea una nueva rama con nombre Vers1 a partir de la rama actual.
Dependiendo de la versión de Git, ejecutamos `git checkout -b Vers1` o para versiones más recientes `git switch -c Vers1`.
![](Images/img37.png)

3. Haz una modificación del index.html y guardas modificaciones.
![](Images/img38.png)

4. Sube los cambios al respositorio remoto a la rama Vers1 `git push origin Vers1` (En este caso podemos ver cómo el index.html de la rama m̀ain y Vers1 son diferentes.
![](Images/img39.png)
![](Images/img40.png)

git add index.html

git commit -m "Modificación del index.html en la rama Vers1"

git push origin Vers1

Para ver las diferencias entre la rama main y Vers1, ejecutamos el comando `git diff main..Vers1`






> Ángel Pérez Blanco
