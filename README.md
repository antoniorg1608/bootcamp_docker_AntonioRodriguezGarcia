# bootcamp_docker_AntonioRodriguezGarcia

Para hacer la imagen en docker:
docker build . -t imagen1
Con esta instrucción descargamos la imagen que hemos creado en nuestro dockerfile y la llamaremos imagen1

docker run -d --name c1 -v miVolumen -p 8080:80 imagen1
Con esta instrucción creamos un contenedor en demonio, con nombre c1, con un volumen llamado miVolumen, corriendo en el puerto 8080 y con la imagen1 que es la que hemos creado.

Con la intrucción docker exec -it c1 bash podremos entrar en nuestro contenedor de forma interactiva, con ls podremos ver los directorios de nuestro contenedor con cd htdocs entraremos dentro de htdocs, si hacemos un ls veremos el archivo index.html y entraremos dentro con la instruccion cat index.html podremos ver la web de Hola con un h1 que pone Hola Mundo.
Si corremos nuestro navegador en localhost:8080 veremos nuestra web con Hola Mundo.

Si ponemos la instruccion docker inspect c1 veremos mucha informacion de nuestro contenedor entre ellas, veremos en la sección Mounts nuestro volumen creado.


