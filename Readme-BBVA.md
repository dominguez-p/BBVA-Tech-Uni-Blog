CRONOLOGÍA DE LA PRÁCTICA:

1.- Crear repositorio GitHub (licencia MIT): https://github.com/dominguez-p/BBVA-Tech-Uni-Blog.git
2.- Clonar repositorio en directorio local /home/alumno/gitlocal/Polymer/
            git clone https://github.com/dominguez-p/BBVA-Tech-Uni-Blog.git
3.- Desde directorio local /home/alumno/gitlocal/Polymer/BBVA-Tech-Uni-Blog iniciamos Polymer 2.0 (starter kit): polymer init
4.- Eliminamos lo no necesario (view1, view2, view3, etc) y nos quedamos con un esqueleto de aplicación Polymer 2.0
5.- Creamos un nuevo elemento Polymer 2.0 (con polymer init) para la Landing Page, eliminando todo lo que genera excepto la página html (home-page.html). Copiamos la página home-page.html en la carpeta /src. Desde my-app.html hacemos referencia al nuevo elemento home-page.html. Subimos los cambios al repositorio Git.
6.- Una vez tenemos lo mínimo (app con home-page) y sin errores (comando polymer lint), empaquetamos la aplicación con el comando
            polymer build --name defalut
7.- Creación del docker:
  7.1.- Clonamos el repositorio (a cualquier ruta local) de alguien que ya tienen un docker con un servidor de aplicaciones nginx:
            git	clone	https://github.com/jlcanela/nginx-openshift-docker-image.git
  7.2.- Copiamos las carpetas etc, usr y el fichero "Dockerfile" a /home/alumno/gitlocal/Polymer/BBVA-Tech-Uni-Blog
  7.3.- Modificamos el fichero "Dockerfile" para que copie nuestros estáticos de la carpeta build/default (generada con polymer build --name default) y para que exponga por el puerto 8082
  7.4.- Desde /home/alumno/gitlocal/Polymer/BBVA-Tech-Uni-Blog creamos el contenedor:
            sudo docker build -t yelpcamp .
  7.5.- Hacemos correr el docker:
            sudo docker run -P --network="host" yelpcamp
  7.6.- Comprobamos que funciona desde varios navegadores: http://localhost:8082
8.- Subimos los cambios al repositorio Git.Subimos los cambios al repositorio Git.
9.- Crear elemento all-campings
  9.1.- Instalar componente iron-ajax
            bower install iron-ajax --save
10.- Subimos los cambios al repositorio Git.
11.- Crear elemento register-login
  11.1.- Instalar componente paper-button, iron-input
            bower install paper-button iron-input --save
12.- Crear el elemento log-out
13.- Crear el elemento new-camping (para crear y editar post)
  13.1.- Instalar el componente iron-autogrow-textarea
            bower install iron-autogrow-textarea --save
14.- Crear el elemento show-camping (para ver el detalle de cada post)          
