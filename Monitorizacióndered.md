# Monitorización de red

### Comando TCPDUMP

Con tcpdump podemos capturar y analizar los paquetes de nuestra red.

[Imagen tcpdump ](Imagen/ImagenesRed/tcpdump.png)

Nos ha capturado los paquetes que salen y entran en nuestra red local.


> tcpdump -i [interfaz]

Con esta opción se especifica la interfaz que se debe capturar.

[Imagen tcpdump -i ](Imagen/ImagenesRed/tcpdump-i.png)

Nos capta los paquetes de la red especificada dándonos una información del tráfico que está pasando por la tarjeta de red.

> tcpdump -D --list-interfaces

Imprime la lista de interfaces de red disponibles en el sistema y en las que tcpdump puede capturar paquetes.  Para cada interfaz red, se imprimen un número y un nombre de interfaz, posiblemente seguidos de una descripción de texto de la interfaz. 

[Imagen tcpdump -D ](Imagen/ImagenesRed/tcpdump-D.png)

Vemos que nos muestra las interfaces de red de nuestra máquina. Nos aparece enp0s3 que es nuestra red lan y virbr0 de una red de kvm.

### Comando TCPTRACK

tcptrack es una herramienta de monitorización en tiempo real
que muestra conexiones TCP activas, direcciones IP origen y
destino, puertos, estado de la conexión y cantidad de datos
transmitidos en un formato visual.

Uso básico > tcptrack -i [nombre-interfaz]

[Imagen tcptrack ](Imagen/ImagenesRed/tcpdump-D.png)

Nos muestra todo el tráfico de nuestra conexión tcp activa en tiempo real.

### Comando IPTRAF-NG

Es una herramienta interactiva que proporciona
estadísticas detalladas sobre el tráfico de red en tiempo real.

Uso básico > iptraf-ng

Nos muestra un menú con las opciones que tenemos.

IMAGEN...

Como se ve en la imagen, podemos monitorear el tráfico de red, filtrar, configurar,etc...

Si le damos a **IP traffic monitor** podemos seleccionar todas las interfaces o solamente de las que tengamos en nuestra máquina, seleccionar la que queramos.

**Configuration**

[Imagen iptraf-ng configuration ](Imagen/ImagenesRed/iptraf-ng-configuration.png)

Podemos cambiar la configuración con las opciones que mejor nos vengan.

Con las opciones que nos ofrece el comando, podemos aplicar especificamente lo que queremos hacer sin pasar por el menú.

### Comando NETSTAT

Es una herramienta clásica para inspeccionar conexiones de red, sockets y estadísticas.

> netstat -a

Muestra los conectores en espera y los que no lo están. Con la opción --interfaces muestra las interfaces inactivas.

[Imagen netstat -a ](Imagen/ImagenesRed/netstat-a.png)

Nos meustra de izquierda a derecha, protocolo, Recv-Q(establecida  (established) la  cantidad  de  bytes no copiados), Send-Q (contabiliza los bytes), Local Adress(La  dirección local (nombre del ordenador local), Foreign Address (dirección y número de  puerto  del  conector  del  sistema  remoto.) y state (el  estado del conector).

> netstat -n

Muestra  direcciones  numéricas  en  vez  de  tratar  de  determinar un sistema, puerto o nombre de usuario.

[Imagen netstat -n ](Imagen/ImagenesRed/netstat-n.png)

Vemos que nos muestra el protocolo, conecctividad, estado, el tipo y el path.

> netstat -tp

Ver conexiones TCP activas con información de procesos.

[Imagen netstat -tp ](Imagen/ImagenesRed/netstat-tp.png)

Vemos las conexiones activas y el puerto por el que se ejecuta. Como vemos tenemos en ejecución firefox.

> netstat -l

Se utiliza para mostrar todos los puertos que están escuchando (en modo "listening") en el sistema.

[Imagen netstat -l ](Imagen/ImagenesRed/netstat-l.png)

Vemos todos los puertos que están en escucha.
