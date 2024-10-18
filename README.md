
# Tarea 3

## 1. Descarga la imagen 'httpd' y comprueba que está en tu equipo

- Descarga la imagen: *sudo docker pull httpd*

    ![Comando Paso1](/img/paso1_1.png)

- Comprueba que está en el equipo: *sudo docker image ls*

    ![Comando Paso1](/img/paso1_2.png)

## 2. Crea un contenedor con el nombre 'dam_web1'

- Crea un contenedor: *docker run -d --name dam_web1 httpd*

    ![Comando Paso2](/img/paso2.png)

## 3. Si quieres poder acceder desde el navegador de tu equipo, ¿que debes hacer?

- Cambiamos el adaptador de la mv a puente

- Paramos el contenedor: *docker stop dam_web1*

- Eliminamos el contenedor: *docker rm dam_web1*

- Lo volvemos a crear asignadole un puerto: *docker run -d --name dam_web1 -p 8000:80 httpd*

    ![Comando Paso3](/img/paso3_1.png)

- Comprobamos que funcione:

    - Comprobamos la ip: *ip address*

        ![Comando Paso3](/img/paso3_2.png)

    - En el navegador: *10.0.9.147:8000*

        ![Comando Paso3](/img/paso3_3.png)

### 3.1 Utiliza bind mount para que el directorio del apache2 'htdocs' esté montado un directorio que tu elijas

- Creamos un nuevo directorio: *sudo mkdir /home/owo/compartidoApache*

- Volvemos a eliminar el directorio

- Lo volvemos a crear con un mount: *docker run -p 8000:80 -v /home/owo/compartidoApache:/usr/local/apache2/htdocs --name dam_web1 httpd
*
    ![Comando Paso3](/img/paso3_1_1.png)

- Comprobamos que funcione:

    ![Comando Paso3](/img/paso3_1_2.png)

## 4. Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador

- Creamos un archivo html en el mount: *sudo nano /home/owo/compartidoApache/index.html*

    ![Comando Paso4](/img/paso4_1.png)

- Comprobamos que funcione:

    ![Comando Paso4](/img/paso4_2.png)
