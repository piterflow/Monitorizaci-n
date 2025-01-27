# Monitorización de almacenamiento

### Comando FREE

> free

El comando free muestra información sobre el uso de la memoria RAM (libre y 	utilizada).

[Imagen Free](Imagen/ImagenesAlmacenamiento/free.png)

Nos muestra una descripción detallada de la memoria, total, usado, libre, compartido, búf/cache, disponible.

> free -h

Nos muestra una salida legible para los usuarios. La información es más detallada, mostrando la memoria en gigabytes y megabytes.

[Imagen free -h ](Imagen/ImagenesAlmacenamiento/free-h.png)
En la memoria baja si tenemos datos, esto se debe a que abarca la capacidad de memoria hasta los 640 k. Sin embargo, la memoria alta no tenemos muestras ya que nos mostraría datos a partir de 640k en adelante.

> free -t

Nos muestra el total de la RAM más intercambio.

[Imagen free -t ](Imagen/ImagenesAlmacenamiento/free-t.png)

Con respecto a las otras opciones mostrada, en ninguna nos muestra el total de la memoria, sin embargo, con está opción nos la muestra.

### Comando DF

El comando df permite conocer el uso y la disponibilidad del espacio en los sistemas de archivos (Espacio de disco libre y utilizado).

> df -h

Nos muestra el tamaño de las particiones en la potencia 1024.

[Imagen df -h ](Imagen/ImagenesAlmacenamiento/df-h.png)

Vemos que el tamaño nos lo muestro en Megas ó Gigas.

> df -t [fichero]

Limita el listado de ficheros al nombre del sistema de fichero

[Imagen df -t ](Imagen/ImagenesAlmacenamiento/df-t.png)

Nos muestro solo los sistemas de ficheros que son tmpfs.

> df -x [fichero]

Limita el listado de sistema de ficheros al tipo de fichero que le pasamos.

[Imagen df -x ](Imagen/ImagenesAlmacenamiento/df-x.png)

En el comando df nos muestra todo los sistemas de ficheros. En el recuadro indicamos que excluya el sistema de ficheros tmpfs por lo que nos muestra todo los sistemas de ficheros menos tmpfs.

### Comando DU
El comando du calcula el espacio que ocupan los directorios y archivos concretos.

> du -h

Muestra el tamaño legible para los usuarios.

[Imagen du -h ](Imagen/ImagenesAlmacenamiento/du-h.png)

Vemos que a la izquierda nos pone el tamaño de los directorios/archivo y a la derecha a que pertenecen.

> du -d [nivel] →  Si indicamos all (nos mostrará todo los archivos que están en primer nivel).

[Imagen du -d ](Imagen/ImagenesAlmacenamiento/du-d.png)

Nos muestra los directorios o archivos que se encuentran en el primer nivel de la jerarquía.. Si indicamos un 2, nos mostrará de segundo nivel.

### Comando IOSTAT

El comando iostat forma parte del paquete sysstat y ofrece información estadística sobre el uso del procesador y la actividad de los dispositivos de almacenamiento. 

> iostat -x

Nos muestra una estadística extendida.

[Imagen iostat -x ](Imagen/ImagenesAlmacenamiento/iostat-x.png)

Nos muestra una estadística extendida de la cpu..

> iostat -d

Muestra el informe de utilización del dispositivo.

[Imagen iostat -d ](Imagen/ImagenesAlmacenamiento/iostat-d.png)

Muestra un informe de utilización de la CPU.

