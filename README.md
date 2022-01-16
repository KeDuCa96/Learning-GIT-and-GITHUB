# Learning-GIT-and-GITHUB
Este es el primer repositorio que creo mientras aprendo GIT y GITHUB. Estaré puliendo los conceptos a medida que voy subiendo los proyectos que he creado en los cursos que he realizado y proyectos propios.


----->  BASICO:

1. Debemos registrarnos en GITHUB https://github.com/ e instalar GIT con  https://git-scm.com/

Luego en consola de VSC:

2.  Registramos nuevos usuarios asociados:

        git config --global user.email "myemail@example.com" ---> Nos puede abrir una ventana dodne nos pedirá identificarnos con un token o desde el browser.

3.  Creamos la primera carpeta oculta para nuestro repositorio. Esto solo lo debemos hacer una vez en todo el proyecto:

        git init  ---> Creamos la carpeta local para iniciar el proyecto.

4.  Revisamos los archivos que hemos creado y los reservamos de manera local.

        git add 'nombreDelArchivo' -->  Con este solo agregamos un archivo en especifico. Luego de darle un add veremos que al lado del nombre de nuestros archivos aparecerá una M en color naranja, esto nos indica que hemos modificado algo.

        git add . ---> agregamos todos los archivos.

        git status -s ---> vemos cuales archivos no han sido agregados. Al ver la lista de archivos veremos que inician con una M de algún color, si la vemos roja es que nos falta darle un git add y si esta verde es que ya podemos darle un git commit.

5.  Creamos una copia momentanea de los archivos ya agregados previamente y con esto podremos viajar en el tiempo.

        git commit -m "primer commit"  ---> si esto se cumple con exito la terminal nos mostrará todo los cambios que se han hecho hasta el momento.

        git log --oneline---> vemos la cantidad de commit que hemos hecho con sus ID. También podremos ver los tag o versiones que hemos hecho y los branch o ramas, pero eso lo vemos un poco mas abajo.

6.  Viajamos a través de los commit con los siguientes tres pasos:
    Con esto podemos restaurar cambios que no hayamos hecho días atrás y no nos gusten, nos creen conflicto en código, etc. Por eso es muy importante que los commit que hagamos estén bien especificados.

        get reset --hard 'idDelCommit' ---> Con este regresamos al commit que querramos. 

        git log --oneline ---> visualizamos los commit y decidimos a cual volver. 

        get reset --hard 'idDelCommit' ---> Con este regresamos al commit que querramos.

7.  Una vez en GITHUB podremos crear un nuevo repositorio y este nos dará una lista de comandos el cual usaremos dos:

        git remote add origin 'urlArrojadaPorGITHUB' ---> con esto podremos trabajar de forma remota.

        git push -u origin master ---> esto solo una vez luego solo podremos usar el git push

8.  Traemos los archivos que creamos directo en el GITHUB

        git pull ---> Esto nos trae los commit que creamos en GITHUB, por ejemplo este README.md fue creado directo en GITHUB y no en VSC.

        git fetch ---> compara los archivos que tengamos local vs en el GITHUB.


----->  TAGS
Se ven reflejados en el apartado de tags y nos sirven para crear versiones del proyecto.

1.  Creamos la primera versión:

        git tag version1.0 -m "descripcion que querramos plasmar en el tag"  ---> creamos la versión


        git log --oneline ---> nos muestra todos los tag o versiones. 

        git push --tags ---> Con esto subimos los tags a la nube o GITHUB

---->   BRANCH
Son líneas de tiempo paralela para luego podemos juntar, todo este tiempo hemos usado la rama MASTER. Trabajando en equipo lo mas seguro es que toque dividir proyecto en diferentes etapas y en algún momento toca unirlos por ejemplo: el front y back trabajan cada uno en su rama y luego se unen. 

1.  Creamos una rama:

        git branch ramaParrafo ---> Creamos la rama, pero aún seguimos en la master.

        git checkout 'nombreDeLaRama' ---> Si nos muestra un switched quiere decir que nos cambiamos de rama.

        git branch ---> Esto nos mostrará la cantidad de ramas y en la que estamos.

2.  Unimos las ramas:
    Hacemos todos los add, commit en nuestra nueva rama
    Posiblemente todas estas indicaciones se vean creadas por la rama front
    
        git checkout 'nombreDeLaRama' ---> nos cambioamos a la rama master

        git branch ---> Verificamos el nombre de las ramas y tenemos que estar en el master 

        git merge 'nombreDeLaRama' ---> con esto hacemos la unión