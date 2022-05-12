# bootcamp_docker_AntonioRodriguezGarcia

Para hacer la imagen en docker:
docker build . -t imagen1
Con esta instrucción descargamos la imagen que hemos creado en nuestro dockerfile y la llamaremos imagen1

Con la instruccion docker volume create miVolumen crearemos nuestro volumen llamado miVolumen.

Para ver que se ha creado correctamente pondremos la instruccion docker volume ls y nos saldrá el volumen creado.

Con la instrucción docker volume inspect miVolumen podremos ver información acerca de nuestro volumen.

Con la instruccion docker run -d --name c1 -v miVolumen:/var/www/html -p 8080:80 imagen1 crearemos nuestro contenedor en demonio llamado c1, corriendo en el puerto 8080:80, con un volumen que se va a llamar miVolumen con su ruta correspondiente dentro de nuestro contenedor, a partir de la imagen1. 

Con la intrucción docker exec -it c1 bash podremos entrar en nuestro contenedor de forma interactiva, con ls podremos ver los directorios de nuestro contenedor con cd htdocs entraremos dentro de htdocs, si hacemos un ls veremos el archivo index.html y entraremos dentro con la instrucción cat index.html podremos ver la web de Hola con un h1 que pone Hola Mundo.

Si corremos nuestro navegador en localhost:8080 veremos nuestra web con Hola Mundo.

Si ponemos la instruccion docker inspect c1 podremos ver tambien toda la información de nuestro contenedor.

