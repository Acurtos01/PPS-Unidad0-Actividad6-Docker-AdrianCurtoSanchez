# Actividad 2

## Servidor Web.

Crearemos un contenedor con el nombre `web` empleando la imagen `php:7.4-apache` siendo accesible en el equipo anfitrion por el puerto `8000`, para ello ejecutaremos el siguiente código:

```
docker run -d -it -p 8000:80 --name web php:7.4-apache
```


## Servidor de base de datos.