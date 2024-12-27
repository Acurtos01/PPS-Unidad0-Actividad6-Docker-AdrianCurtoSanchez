# Actividad 6

## Creación de una imagen a partir de un contenedor 

1. Ejecutamos un container de Debian con `docker run -it --name contenedor-1 debian bash`.
![Docker run](../images/actividad-6/docker-run.png)

2. Una vez dentro del contenedor ejecutamos `apt update && apt install inetutils-ping iproute2 dnsutils -y` para intalar paquetes.
![Apt](../images/actividad-6/apt.png)
 
3. Creamos una nueva imagen a partir de `contenedor-1` ejecutando `docker commit contenedor-1 acurtos01/comandos_redes`.
![Docker commit](../images/actividad-6/docker-commit.png)

4. Subimos la imagen a Docker Hub con el comando `docker push acurtos01/comandos_redes`
![Docker push](../images/actividad-6/docker-push.png)
![Dockerhub](../images/actividad-6/dockerhub.png)
5. Descargamos la imagen en otro equipo con el comando `docker pull acurtos01/comandos_redes` y ejecutarla con `docker run -it --name my-image acurtos01/comandos_redes`.
![Docker pull](../images/actividad-6/docker-pull.png)
![Docker run image](../images/actividad-6/docker-run-image.png)