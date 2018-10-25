# mean_docker_demo
Repositorio para usar como demo en la creación de una aplicación basada en MEAN y dockerizada.

## Comandos docker básicos

>Bajar una nueva imagen desde [Docker Store](https://store.docker.com/)
``` 
docker pull nombre_imagen 
```
>Crear una nueva imagen con nuestros sistemas
```
docker build -t mi_imagen directorio_Dockerfile
```
>Ejecutar una imagen
```
docker run -d HostPort:ContainerPort --name mi_container_app mi_imagen 
```
