# mean_docker_demo
Repositorio para usar como demo en la creación de una aplicación basada en MEAN y dockerizada.

## docker - comandos básicos

### Creación y ejecución de imágenes

#### pull
>Bajar una nueva imagen desde [Docker Store](https://store.docker.com/)
``` 
docker pull nombre_imagen 
```
#### build
>Crear una nueva imagen con nuestros sistemas
```
docker build -t mi_imagen directorio_Dockerfile
```
#### run
>Ejecutar una imagen
```
docker run -d HostPort:ContainerPort --name mi_container_app mi_imagen 
```
>Ejecutar con volumen vinculado (tiene que estar vacía la carpeta contenedor)
```
docker run -d -p 9000:9000 -v C:\Temp\content:c:\site --name mi_container_app  mi_imagen
```
### Monitoreo
#### images
>Lista todas las imagenes instaladas
```
docker images 
docker image ls
```
#### ps
>Lista todas las instancias creadas
```
docker ps -a
```
#### inspect
>Obtiene información de la instancia, como ser ip, carpetas compartidas y puerto compartido.
```
docker inspect mi_container_app 
```
>Para obtener solo el IP
```
docker inspect -f "{{ .NetworkSettings.Networks.nat.IPAddress }}" mi_container_app 
```
### Mantenimiento

#### rm
>Eliminar un contenedor (-f para detenerlos)
```
docker rm mi_container_app -f
```
#### rmi
>Eliminar una imagen
```
docker rmi mi_imagen
```
#### image
>Eliminar imagenes colgadas
```
docker image prune
```


### Interactuar con el contenedor

#### exec
>Entrar en modo consola en la instancia (modo interactivo)
```
docker exec -i mi_container_app cmd
```

