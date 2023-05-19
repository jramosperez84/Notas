## Descripción:

Docker es una plataforma de contenedores de software que permite a los desarrolladores empaquetar una aplicación junto con todas sus dependencias en un contenedor virtual que puede ser ejecutado en cualquier sistema operativo. Esto hace que sea más fácil para los desarrolladores crear, enviar y ejecutar aplicaciones en diferentes entornos, ya sea en la nube, en servidores locales o en máquinas de los usuarios. Docker se ha convertido en una herramienta popular en la comunidad de desarrollo de software, ya que permite la portabilidad de las aplicaciones y la creación de entornos de desarrollo más consistentes y reproducibles.

## Comandos utiles:

### Comandos de gestión de imágenes:

-   `docker images`: Lista las imágenes descargadas en el sistema.
-   `docker pull`: Descarga una imagen desde un repositorio de Docker.
-   `docker build`: Construye una imagen a partir de un archivo Dockerfile.
-   `docker push`: Sube una imagen al repositorio de Docker.

### Comandos de gestión de contenedores:

-   `docker ps`: Lista los contenedores en ejecución.
-   `docker run`: Ejecuta un contenedor a partir de una imagen.
-   `docker start`: Inicia un contenedor detenido.
-   `docker stop`: Detiene un contenedor en ejecución.
-   `docker restart`: Reinicia un contenedor.
-   `docker rm`: Elimina un contenedor.

### Comandos de gestión de redes:

-   `docker network ls`: Lista las redes creadas en Docker.
-   `docker network create`: Crea una red en Docker.
-   `docker network connect`: Conecta un contenedor a una red.
-   `docker network disconnect`: Desconecta un contenedor de una red.

### Comandos de gestión de volúmenes:

-   `docker volume ls`: Lista los volúmenes creados en Docker.
-   `docker volume create`: Crea un volumen en Docker.
-   `docker volume rm`: Elimina un volumen de Docker.

### Otros comandos útiles:

-   `docker exec`: Ejecuta un comando en un contenedor en ejecución.
-   `docker logs`: Muestra los logs de un contenedor.
-   `docker inspect`: Muestra información detallada de un contenedor o imagen.
-   `docker-compose`: Gestiona múltiples contenedores como una aplicación.

Es importante tener en cuenta que existen muchos otros comandos en Docker, pero estos son los más comúnmente utilizados. Recuerda que para obtener más información sobre un comando específico, puedes usar el flag `-h` o `--help`.

### Comandos de gestión de imágenes:

- `docker images`: Lista las imágenes descargadas en el sistema.

```bash
docker images
```

- `docker pull`: Descarga una imagen desde un repositorio de Docker.

```bash
docker pull ubuntu
```

- `docker build`: Construye una imagen a partir de un archivo Dockerfile.

```bash
docker build -t mi-imagen
```

- `docker push`: Sube una imagen al repositorio de Docker.

```bash
docker push mi-repositorio/mi-imagen
```

### Comandos de gestión de contenedores:

-   `docker ps`: Lista los contenedores en ejecución.

```bash
docker ps
```

- `docker run`: Ejecuta un contenedor a partir de una imagen.

```bash
docker run -it --name mi-contenedor ubuntu
```

- `docker start`: Inicia un contenedor detenido.

```bash
docker start mi-contenedor
```

- `docker stop`: Detiene un contenedor en ejecución.

```bash
docker stop mi-contenedor
```

- `docker restart`: Reinicia un contenedor.

```bash
docker restart mi-contenedor
```

- `docker rm`: Elimina un contenedor.

```bash
docker rm mi-contenedor
```

### Comandos de gestión de redes:

- `docker network ls`: Lista las redes creadas en Docker.

```bash
docker network ls
```

- `docker network create`: Crea una red en Docker.

```bash
docker network create mi-red
```

- `docker network connect`: Conecta un contenedor a una red.

```bash
docker network connect mi-red mi-contenedor
```

- `docker network disconnect`: Desconecta un contenedor de una red.

```bash
docker network disconnect mi-red mi-contenedor
```

### Comandos de gestión de volúmenes:

- `docker volume ls`: Lista los volúmenes creados en Docker.

```bash
docker volume ls
```

- `docker volume create`: Crea un volumen en Docker.

```bash
docker volume create mi-volumen
```

- `docker volume rm`: Elimina un volumen de Docker.

```bash
docker volume rm mi-volumen
```

### Otros comandos útiles:

- `docker exec`: Ejecuta un comando en un contenedor en ejecución.

```bash
docker exec -it mi-contenedor bash
```

- `docker logs`: Muestra los logs de un contenedor.

```bash
docker logs mi-contenedor
```

- `docker inspect`: Muestra información detallada de un contenedor o imagen.

```bash
docker inspect mi-contenedor
```

- `docker-compose`: Gestiona múltiples contenedores como una aplicación.

```bash
docker-compose up
```

[Documentacíon oficial](https://docs.docker.com/)

[Volver](/Herramientas_de_desarrollo.md)