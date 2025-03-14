
Creamos un Dockerfile personalizado y luego construir una imagen a partir de ese Dockerfile. Luego, puedes ejecutar un contenedor basado en esa imagen. Aquí hay un ejemplo de cómo hacerlo:

Paso 1: Crear un Dockerfile
Crea un archivo llamado "Dockerfile" en el directorio de tu proyecto con el siguiente contenido:

```Dockerfile
# Usa la imagen base de MariaDB
FROM MariaDB:latest

# Establece las variables de entorno necesarias
ENV MARIADB_ROOT_PASSWORD:'root'
ENV MARIADB_DATABASE:'example'
ENV MARIADB_USER:'example'
ENV MARIADB_PASSWORD:'example'

# Expone el puerto 3306
EXPOSE 3306
```

Paso 2: Construir la imagen
Abre una terminal en el directorio donde se encuentra tu Dockerfile y ejecuta el siguiente comando para construir la imagen:

```bash
docker build -t mariadb-image-latest .
```

Reemplaza "mariadb-image-latest" con el nombre que desees para tu imagen.

Paso 3: Ejecutar un contenedor
Una vez que la imagen se haya construido con éxito, puedes ejecutar un contenedor basado en esa imagen con la configuración deseada. Puedes usar el comando `docker run` para hacerlo:

```bash
docker run -d --name mariadb-container -p 3306:3306 -v db:/var/lib/mariadb mariadb-image-latest
```

Esto creará un nuevo contenedor llamado "mariadb-container " basado en la imagen que acabas de construir y utilizará la configuración de variables de entorno y volúmenes que especificaste en tu Dockerfile.

Ahora deberías tener un contenedor en funcionamiento.

# Elminar contenedor e imagen
```bash
docker rm -f mariadb-container; docker rmi mariadb-image-latest
```
# Elminar contenedor e imagen y reCrear y arrancar
```bash
docker rm -f mariadb-container; docker rmi mariadb-image-latest; docker build -t mariadb-image-latest . ; docker run -d --name mariadb-container -p 3306:3306 -v db:/var/lib/mariadb mariadb-image-latest
```