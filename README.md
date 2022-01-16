# Learning-GIT-and-GITHUB
Este es el primer repositorio que creo mientras aprendo GIT y GITHUB. Estaré puliendo los conceptos a medida que voy subiendo los proyectos que he creado en los cursos que he realizado y proyectos propios.


1. Debemos registrarnos en GITHUB https://github.com/

2. Registramos nuevos usuarios asociados:

    git config --global user.email "myemail@example.com"

3.  Creamos la primera carpeta oculta para nuestro repositorio. Esto solo lo debemos hacer una vez en todo el proyecto.

    git init  ---> Creamos la carpeta local para iniciar el proyecto.

4. Agregamos los archivos que hemos creado con

    Revisamos los archivos que hemos creado y los reservamos de manera local.

    git add <nombreDelArchivo> -->  Con este solo agregamos un archivo en especifico.

    git add . ---> agregamos todos los archivos.

    get status -s ---> vemos cuales archivos no han sido agregados.

5. Creamos una copia momentanea de los archivos ya agregados previamente y con esto podremos viajar en el tiempo.

    git commit -m "primer commit"   

    git log --oneline---> vemos la cantidad de commit que hemos hecho.

6. Viajamos a través de los commit con los siguientes tres pasos:

    get reset --hard <idDelCommit> ---> Con este regresamos al commit que querramos. 

    git log --oneline ---> visualizamos los commit y decidimos a cual volver 

    get reset --hard <idDelCommit> ---> Con este regresamos al commit que querramos. 
    



