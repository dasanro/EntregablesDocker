Se ha creado una aplicación que lee los datos de la base de datos, y los devuelve en un formato de json.

Para poder ver su funcionamiento debemos de ejecutar en un terminal el siguiente comando, tras haber descargado el contenido.

docker-compose up

Una vez desplegado, en el navegador web, nos dirigimos a la web:
http://localhost:5000/

Y nos aparecen los datos que hemos cargado en la web y son 
{"favorite_colors": [{"Lancelot": "blue"}, {"Galahad": "yellow"}]}