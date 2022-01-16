# Learning-GIT-and-GITHUB
Este es el primer repositorio que creo mientras aprendo GIT y GITHUB. Estaré puliendo los conceptos a medida que voy subiendo los proyectos que he creado en los cursos que he realizado y proyectos propios.


1. Debemos registrarnos en GITHUB https://github.com/ e instalar GIT con  https://git-scm.com/

Luego en consola de VSC:

2. Registramos nuevos usuarios asociados:

    git config --global user.email "myemail@example.com" ---> Nos puede abrir una ventana dodne nos pedirá identificarnos con un token o desde el browser.

3.  Creamos la primera carpeta oculta para nuestro repositorio. Esto solo lo debemos hacer una vez en todo el proyecto.

    git init  ---> Creamos la carpeta local para iniciar el proyecto.

4. Agregamos los archivos que hemos creado con

    Revisamos los archivos que hemos creado y los reservamos de manera local.

    git add <nombreDelArchivo> -->  Con este solo agregamos un archivo en especifico. Luego de darle un add veremos que al lado del nombre de nuestros archivos aparecerá una M en color naranja, esto nos indica que hemos modificado algo.

    git add . ---> agregamos todos los archivos.

    get status -s ---> vemos cuales archivos no han sido agregados. Al ver la lista de archivos veremos que inician con una M de algún color, si la vemos roja es que nos falta darle un git add y si esta verde es que ya podemos darle un git commit

5. Creamos una copia momentanea de los archivos ya agregados previamente y con esto podremos viajar en el tiempo.

    git commit -m "primer commit"   

    git log --oneline---> vemos la cantidad de commit que hemos hecho.

6. Viajamos a través de los commit con los siguientes tres pasos:

    get reset --hard <idDelCommit> ---> Con este regresamos al commit que querramos. 

    git log --oneline ---> visualizamos los commit y decidimos a cual volver 

    get reset --hard <idDelCommit> ---> Con este regresamos al commit que querramos. 

7. Una vez en GITHUB podremos crear un nuevo repositorio y este nos dará una lista de comandos el cual usaremos dos:

    git remote add origin <urlArrojadaPorGITHUB> ---> con esto podremos trabajar de forma remota.

8. Para finalizar y poder visualizar nuestros cambios en GITHUB 

    git push -u origin master ---> esto solo una vez luego solo podremos usar el git push

