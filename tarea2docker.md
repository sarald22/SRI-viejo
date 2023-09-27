# Sara Lamas ASIR2

## Tarea: Docker - Trabajando con volúmenes


1. **Descarga la imagen 'httpd' y comprueba que está en tu equipo.**

  hecho 


2. Crea un contenedor con el nombre 'asir httpd'.
   
   añadimos estas líneas al archivo “docker-compose.yml”

      services:
        asir_httpd:
          image: httpd:2.4
          ports:
            - "80:80"
          volumes:
            - /home/asir2/SRI/APACHE/paginas
          container_name: asir httpd


   luego en terminal enviamos este comando, para crear el contenedor:

      docker run -dit --name my-apache-app -p 8080:80 -v /home/asir2/SRI/APACHE/paginas:/usr/local/apache2/htdocs/ httpd:2.4

