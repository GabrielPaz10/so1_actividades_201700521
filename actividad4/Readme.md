## Actividad 4 201700521

1. Se debe crear un archivo con extension .service en esta ruta ```  /etc/systemd/system ```
2. El contenido del archivo sera el siguiente:
   ```
   [Unit]
    Description=Hola Mundo Service

    [Service]
    Type=simple
    ExecStart=/bin/bash /home/Gabriel10/script.sh

    [Install]
    WantedBy=multi-user.target
   ```
3. En script.sh iria el siguiente codigo:
   ```
   while true; do
    echo "Hola Mundo!"
    sleep 5
    done
   ```
4. Para activar el servicio se hace de la siguiente manera:
   ``` sudo systemctl enable holamundo.service ```
5. Para iniciar el servicio es con el siguiente comando:
   ``` sudo systemctl start holamundo.service ```


### Instalacion y uso del servicio

1. Para activar el servicio seria de esta forma:
   ``` sudo systemctl start holamundo.service ```
2. Para detener el servicio:
   ``` sudo systemctl stop holamundo.service ```

3. Para verificar el estado del servicio:
   ``` sudo systemctl status holamundo.service ```
   La salida seria como la siguiente:
   ```
   holamundo.service - Hola Mundo Service
   Loaded: loaded (/etc/systemd/system/holamundo.service; enabled; vendor preset: enabled)
   Active: active (running) since Thu 2023-08-31 23:32:53 KST; 2min 36s ago
   Process: 1015 ExecStart=/bin/bash /path/to/script.sh (code=exited, status=0/SUCCESS)
   Main PID: 1015 (bash)
    Tasks: 1 (limit: 15239)
   CGroup: /system.slice/holamundo.service
           └─1015 /bin/bash /path/to/script.sh

    Aug 31 23:32:53 myserver systemd[1]: Starting Hola Mundo Service...
    Aug 31 23:32:53 myserver systemd[1]: Started Hola Mundo Service.
   ```
