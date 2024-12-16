# Actividad 2

## Servidor Web.

Crearemos un contenedor con el nombre `web` empleando la imagen `php:7.4-apache` siendo accesible en el equipo anfitrion por el puerto `8000`, para ello ejecutaremos el siguiente código:
```
docker run -d -p 8000:80 --name web php:7.4-apache
```
![Docker run](../images/actividad-2/docker-run.png)

Accedemos a la terminal del contendor con el siguiente comando:
```
docker exec -it web bash
```
![Docker exec](../images/actividad-2/docker-exec.png)

Estando en la terminal del contenedor creamos el fichero index.html con el siguiente comando:
```
print "<h1>Hola soy Adrián Curto</h1>" > index.html
```

Y tambien deberemos crear el fichero index.php con el siguiente comando:
```
touch "<?php echo phpinfo(); ?>" > index.php
```


## Servidor de base de datos.