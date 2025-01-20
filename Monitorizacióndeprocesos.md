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

'''top -c'''
Alterna la columna COMMAND entre mostrar el comando o el nombre del programa.
