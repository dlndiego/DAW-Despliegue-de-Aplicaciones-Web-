# PROYECTO APACHE

## FASE 1

`ENUNCIADO:`

Fase 1. Instalación y estructura
1. Instalar Apache 2.4 y comprobar el servicio con systemctl status apache2 y apache2ctl -v.
2. Crear la estructura de directorios: /var/www/verdemar/public y /var/www/verdemar/intranet, con propietario www-data y permisos mínimos necesarios (directorios 755, ficheros 644).
a. sudo find /var/www/prueba.com -type d -exec chmod 755 {} \;
b. sudo find /var/www/prueba.com -type f -exec chmod 644 {} \;
3. Desactivar el sitio por defecto y el módulo o configuración que no se use

`RESULTADO:`

Hemos dado los permisos, hemos desactivados los demas sitios y hemos reiniciado el servicio de apache.

![](IMG/FASE1.png)

## FASE 2 

`ENUNCIADO:`

Fase 2. Hosts virtuales por nombre
1. Un fichero .conf por sitio en sites-available, activado con a2ensite. Nada de modificar 000-default.conf ni meter todo en apache2.conf.
2. ServerName, ServerAdmin, DocumentRoot, ErrorLog y CustomLog propios para cada sitio.
3. Acceso desde otro equipo (o desde el anfitrión) por nombre, con las entradas necesarias en /etc/hosts o servidor DNS.

`RESPUESTA:`

La primera pagina despues de cambiar `etc/hosts`:
![](IMG/pag1Fase2.png)

La segunda pagina despues de cambiar `etc/hosts`:
![](IMG/pag2Fase2.png)

## FASE 3

`ENUNCIADO:`

Fase 3. HTTPS y redirecciones
1. Generar un certificado autofirmado con openssl que incluya ambos dominios, con clave de 2048 bits como mínimo.
2. Publicar ambos sitios en el puerto 443.
3. Redirigir todo el tráfico HTTP (80) a HTTPS con 301.
4. Redirigir verdemar.local (sin www) a www.verdemar.local.

`RESPUESTA:`

Despues de activar y configurar todo el `https`:
![](IMG/FASE3COMPROBACION1.png)