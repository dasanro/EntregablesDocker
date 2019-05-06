Antes de comenzar, debemos de configurar el fichero de hosts que encontramos en la ruta:

sudo vim /etc/ansible/hosts

Seguidamente creamos la carpeta en la que deseamos realizar el despliegue.

mkdir python-mysql
cd python-mysql

Ahora creamos el fichero de hosts y el playbook.

touch hosts site.yml
touch playbook.yml
mkdir -p roles/
cd roles/

Dentro del directorio de roles, ejecutamos el siguiente comando en donde (app, hace referencia al nombre del rol)

ansible-galaxy init app
ansible-galaxy init db

Dentro de la ruta roles/app/files copiamos nuestro fichero app.py que sera ejecutado al inicio.

Vamos a configurar los ficheros situados en:
+ /roles/app/tasks/main.yml con la configuración a realizar por la parte de python
+ /roles/db/tasks/main.yml con la parte de la base de datos.
+ /roles/db/vars/main.yml con los datos de usuario, contraseña de la base de datos.

Final para ejecutarlo, nos situamos en el directorio raiz y ejecutamos:
ansible-playbook -i hosts site.yml 

