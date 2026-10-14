# DOCKER

### PUNTO 1A

Crea y ejecuta un contenedor a partir de la imagen de nginx con las siguientes
características:

**● Nombre: webserver.**
**● Mapeo de puertos: el 80 del contenedor al 8080 del anfitrión.**
**● Que se ejecute en segundo plano.**


![](img/crearContenedor.png)

```bash
docker run  # Crea y arranca un contenedor.
-d # Para que se ejecute en segundo plano.
--name webserver # Asignarle el nombre a el contenedor.
-p 8080:80 #Definimos el puerto.
nginx #La imagen que vamos a usar (Si no existe se descarga automaticamente).
docker ps # Verificamos que esta funcionando.
```

Accede a la web desde Firefox para que se vea.

![](img/accediendoAlContenedor.png)

---

### PUNTO 1B

Ahora abre un terminal interactivo con el contenedor y cambia la página web que
se ve por defecto, que está en “/usr/share/nginx/html” por una que muestre un
título y una imagen.

La imagen tendrás que copiarla desde el anfitrión al contenedor y meterla en la
carpeta correspondiente para que se vea en la web.

Aqui copiamos la imagen, y la metemos dentro del contenedor.
![alt text](img/copiarImagen.png)

Abrimos la linea de comandos del contenedor webserver, nos movemos a la ruta donde tenemos el html y la foto copiada anterior mente y cpn el cat suministramos el codigo HTML que yo lo he sacado de internet.

![alt text](img/modificandoHTML.png)

Al buscar la pagina desde el **FIREFOX** y se ve asi

![alt text](img/paginaModificada.png)

### PUNTO 2

Utilizando las imágenes oficiales de Docker de Wordpress y MySQL monta una
página web con Wordpress funcional.
Después añade un contenedor con phpmyadmin que permita la administración de
la base de datos.

Creamos una **RED**
![alt text](img/crearRed.png)

Creamos un contenedor de **MYSQL**
![alt text](img/contendorMYSQL.png)

```php
MYSQL_ROOT_PASSWORD	#Contraseña del usuario administrador (root)
MYSQL_DATABASE	#Crea automáticamente la base de datos wordpress
MYSQL_USER / MYSQL_PASSWORD	#Crea un usuario normal para WordPress
```

Ahora vamos a crear el contenedor de wordprees, le asignamos la red el nombre y los parametros que aparecen en la captura: 
![alt text](img/crearWordpress.png)

Ahora dede **FIREFOX** hemos entrado al puerto 80 y nos visualiza el wordprees
![alt text](img/vistaWordpres.png)

Y ahora entramos a el puerto 81 y vemos el **phpMyAdmin**
![alt text](img/vistaPHP.png)