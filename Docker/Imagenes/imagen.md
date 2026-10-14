# `IMAGENES EN DOCKER`

---

>`docker images`: Lista todas las imagenes locales.
>`docker images [REPOSIORIO[:ETIQUETA]]`: Filtra las imagenes sobre el repo y la etiqueta que pongas.
>`docker search TERM`: Filtras la informacion sobre esa imagen.
>`docker search -f start = 50`: Filtra por condiciones o contextos.
>`docker search --limit 24`: Esto limita los resultados a 24 (por ejemplo). 
>`docker pull [repositorio]`: Esto es para descargar una imagen.
>`docker history IMAGE[:TAG]`: Ver todo el historial/capas
>`docker rmi IMAGE[:TAG]`: Eliminar una imagen local.
>   >Solo se pueden eliminar imágenes que no tengan     contenedor asociado, a menos que se use la opción -f. 
>
>`docker system prune -a`: Elimina imagenes y contenedores parados.
>`docker commit [opciones] id/name [REPOSITORY[:TAG]]`: Para convertir un contenedor en una imagen. 
>`docker commit -a “Autor” -m “Mensaje” id/name REPOSITORY[:TAG]]`: Para convertir un contenedor en una imagenes pero de manera mas *PROFESIONAL*.
>`docker save IMAGE > archivo.tar`: Para exportar o importar archvos
>
>
>
>
