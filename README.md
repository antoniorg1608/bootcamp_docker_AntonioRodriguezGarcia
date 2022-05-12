# bootcamp_docker_AntonioRodriguezGarcia

Para hacer la imagen en docker:
docker build . -t imagen1
Con esta instrucción descargamos la imagen que hemos creado en nuestro dockerfile y la llamaremos imagen1

docker run -d --name c1 -v miVolumen -p 8080:80 imagen1
Con esta instrucción creamos un contenedor en demonio, con nombre c1, con un volumen llamado mi volumen, corriendo en el puerto 8080 y con la imagen1 que es la que hemos creado.
