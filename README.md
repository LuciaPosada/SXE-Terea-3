
# Tarea 3

## 1. Descarga la imagen 'httpd' y comprueba que está en tu equipo

- Descarga la imagen: *sudo docker pull httpd*

    ![Comando Paso1](/img/paso1_1.png)

- Comprueba que está en el equipo: *sudo docker image ls*

    ![Comando Paso1](/img/paso1_2.png)

## 2. Crea un contenedor con el nombre 'dam_web1'

- Crea un contenedor: *dockerrun -d --name dam_web1 -p 8000:80 httpd*

    ![Comando Paso2](/img/paso2.png)
