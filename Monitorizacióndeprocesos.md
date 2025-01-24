# Monitorización de procesos

Para la monitorización de procesos tenemos el comando top. Nos da una información en tiempo real de los procesos que consumen más recursos.

|OPciones|Descripción|
|------|--------------|
| PID | ID del proceso (Unique Positive Integer) |
| USER | Nombre del usuario que ejecuta el proceso |
| PR | Prioridad (del Kernel) |
| NI | Valor Nice |
| VIRT | Memoria Virtual |
| RES | Tamaño residente (memoria física) |
| SHR | Memoria compartida |
| S | Estado del proceso (Running, Stopped, etc.) |
| %CPU | Carga de CPU |
| %MEM | Porcentage de RES / Total RAM |
| TIME + | Tiempo total empleado en el proceso |
| COMMAD | Comando que inició el proceso |

De los siguientes comandos veremos una pequeña descripción de sus opciones e imagenes.

## Comando TOP.

> top -c

Alterna la columna COMMAND entre mostrar el comando o el nombre del programa.

  [top -c: ](Imagenes/top-c.png)

Como vemos en la imagen, va alternando mostrando el comando que se está utilizando y el nombre del programa en ejecución.

> top -u “Nombre_usuario

 Muestra sólo los procesos del usuario especificado. Esto es útil para filtrar la salida 	y ver sólo los procesos de un usuario en particular.

 IMAGEN...

 Como se ve en la imagen solo muestra el nombre del usuario introducido.

> top -p [PID] -> PID es el ID del proceso

Permite monitorear un proceso específico utilizando su ID de proceso (PID). Esto es útil si deseas centrarte en un proceso en particular sin distraerte con otros.

Ejemplo -> top -p 1742

IMAGEN...

Nos muestra solamente el proceso que hemos introducido como parámetro.

> Top -b “> nombre_archivo”

Inicia top en modo "batch", lo que significa que la salida se puede redirigir a un archivo o a otro comando. Este modo es útil para crear informes.

IMAGEN...

Redireccionamos la salida del comando a un archivo informe.txt.

Visualizamos el contenido con un cat y vemos que se ha redireccionado todo lo que nos mostraría por terminal a un archivo donde nosotros posteriormente podremos filtrar para visualizar los procesos de distinta forma.

> top -d [segundos]

Ejemplo -> top -d 240 (actualizará en “4 minutos”)

Cambia el intervalo de actualización de la pantalla en segundos. Por defecto, top actualiza cada 3 segundos, pero puedes ajustar este valor para ver la información con más o menos frecuencia.

iMAGEN...

En la imagen no se aprecia, para ello tienes que probarlo en tu terminal, y ver que los profesos no cambian hasta pasado el máximo de segundos metido por parámetro.

>  top -i

Invierte el último estado 'i' recordado.

IMAGEN...

Como vemos solo muestra los últimos estados ejecutados.

## Comando HTOP.

Es similar al comando top, nos permite desplazarnos verticalmente y horizontalmente, e interactuar utilizando el ratón. Nos permite visualizar todos los procesos con un argumento de línea de comando así como verlo en formato de árbol, seleccionar varios procesos a la vez y actuar sobre ellos.

No es como el comando top, que todas las opciones tenemos que introducirlas por consola. Con htop ejecutamos y dentro tenemos una serie de opciones que van desde F1 a F9.
Sin embargo, sí es verdad que htop nos da varias opciones para introducir por consola, aunque su funcionalidad reside en los F”número”.

> F1 (Help)

Muestra la ayuda y las instrucciones sobre las funciones de htop.

IMAGE....

Una opción muy útil para principiantes que están aprendiendo a utilizar htop.

> F3

Permite buscar procesos específicos por nombre. Esto facilita encontrar un proceso en una lista extensa.

Indicamos el proceso que queremos buscar y vemos que nos ha mostrado todos los procesos que están ejecutándose con /usr.

> F4

Filtra los procesos en la lista según un criterio específico. Esto es útil para 	concentrarse en un conjunto particular de procesos.

IMAGEN...

Muestra el proceso que está corriendo.

> F5

Cambia la visualización a modo de árbol, mostrando la jerarquía de procesos y sus relaciones parentales.

IMAGEN...

Vemos como en el apartado COMMAND nos muestra en forma de árbol en forma de jerarquía.

> F6

Permite cambiar el criterio de ordenamiento de la lista de procesos (por	 	CPU, memoria, tiempo, etc.).

IMAGEN...

Vemos como en la parte izquierda nos coloca para ordenar según qué proceso. Con la frecha se arriba y abajo podemos movernos o señalando con el ratón.

> F9

Ofrece la opción de enviar una señal a un proceso seleccionado, como terminarlo o enviarle una señal específica.

IMAGEN...

En la parte izquierda podemos seleccionar a cuál proceso queremos mandarle una señal, como por ejemplo, matar proceso.

## Comando PS.

Nos proporciona una instantánea de los procesos en ejecución.

> ps -e

Muestra todos los procesos.

IMAGEN...

Como vemos nos muestra todos los procesos pero no podemos filtrarlos como con htop o top.

>  ps -f

Nos mostrará una lista completa con más detalles.

IMAGEN...

Vemos que ahora nos muestra PPID, C, STIO y el UID.

> ps -l

 Nos muestra una lista más larga y detallada.

IMAGEN...

Ahora nos muestra el PRI, NI, ADDR, SZ, WCHAN.

> ps -aux

Muestra todos los procesos en un formato detallado.

IMAGEN...

Comparado con las otras opciones, nos muestra mucho más procesos.

## Comando ATOP.

> atop -c

Muestra la línea de comandos por proceso.

IMAGEN...

Vemos que nos está mostrando la línea de comando por los procesos que se están ejecutando como /usr/…

> atop -m

Muestra la información relacionada con la memoria.

IMAGEN...

Toda la información que nos muestra tiene relación con la memoria.

> atop -n

Muestra la información de la red.

IMAGEN..

Nos muestra el nombre de nuestra red enp0s3, network, transport.

> atop -y

Nos muestra los hilos individuales.

IMAGEN...

En la imagen vemos que nos identifica los distintos hilos y nos lo señala con distinto color.

