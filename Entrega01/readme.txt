Una vez que hemos descargado los ficheros, debemos de ejecutar primero el siguiente comando, para crear la aplicación. 

Nos situaremos dentro de la carpeta de los archivos que hemos descargado desde un terminal.

Pondremos sudo al inicio, en el caso de no tener permisos de administrador en nuestro usuario.

sudo docker build --tag servidor-flask .

Seguidamente arrancaremos la aplicacion

sudo docker run --name app-python -p 5000:5000 servidor-flask

Ahora podemos ir a un navegador web, y poner la direccion localhost:5000 y podremos ver la ejecución de la aplicación.

Este contenedor se ha publicado *docker hub* y lo podemos encontrar en la siguiente dirección.
https://hub.docker.com/r/dasanro/python-flask

Podemos hacer uso mediante el siguiente comando.
docker pull dasanro/python-flask