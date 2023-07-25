# Kernel
El Kernel se define como el nucleo del sistema operativo
y se encarga de mediar entre los procesos de usuario y el hardwware
disponible de la maquina. Quiere decir que provee de hardware al software que lo necesita. 
Tambien se encarga de dar permisos, facilitar comunicacion entre programas, gestionar diversos labores de un dispositivo manejar el procesador, perifericos y almacenamiento del sistema. 

## Tipos de Kernel
* Microkernel o micronucleo: se basa en ofrecer las funciones básicas de cada dispositivo, administrando aquello que tenga CPU, memoria e IPC. Esto supone un mayor control de dispositivos
* Nucleos Monoliticos: se trata de un gran nucleo informatico para todas las tareas del sistema. Es de tipo no modular y puede alcanzar un mayor rendimiento que un microkernel.
* Nucleos Hibridos: incluyen un código adicional en el núcleo para que se ejecuten labores más rápidamente. Se puede elegir qué acciones ejecutar en modo usuario, y cuáles en modo supervisor.

### Que tipo de Kernel utiliza Linux? 
El núcleo de Linux es monolítico, por lo que los programas tienen mayor acceso al hardware y mantienen mejor comunicación entre sí, pero tiene dificultades a nivel de seguridad. Utiliza los llamados módulos de Kernel para agregar o quitar características del núcleo en el momento en que se necesite.

## User vs Kernel Mode

* User Mode: cuando se inicia un programa en un sistema operativo se inicia el programa en modo de usuario. Los programas de modo de usuario tienen menos privilegios que las aplicaciones de modo de usuario y no se les permite acceder a los recursos del sistema directamente.
* Kernel Mode: Cuando los programas que se ejecutan en modo de usuario necesitan acceso al hardware, por ejemplo, una cámara web, primero tiene que pasar por el núcleo mediante una llamada al sistema y, para llevar a cabo estas solicitudes, la CPU cambia del modo de usuario al modo de núcleo en el momento de la ejecución. Después de completar finalmente la ejecución del proceso, la CPU vuelve a cambiar al modo de usuario .

![Usuario vs Kernel Mode](https://media.geeksforgeeks.org/wp-content/uploads/20220106132002/Uservskernelmode-660x371.png)