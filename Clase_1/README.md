## Actualizar sistema
Se actualiza el sistema operativo con los siguientes comandos
```bash
sudo apt update
sudo apt upgrade
```

## Instalar Webots
Para la instalacion de webots se sigue los siguientes pasos
Agregar la llave de isntalacion
```bash
wget -qO- https://cyberbotics.com/Cyberbotics.asc | sudo apt-key add -
```
Luego, se configura los packages APT, ejecutar las siguientes lineas de comando

```bash
sudo apt-add-repository 'deb https://cyberbotics.com/debian/ binary-amd64/'
sudo apt-get update
```

Finalmente instalar Webots con el siguiente comando
```bash
sudo apt-get install webots
```
Instalacion directa desde un package Debian (extension .deb)
Descargar el archivo . deb del siguiente [link](https://cyberbotics.com/#download):

En la Ubicacion del archivo ejecutar el siguiente comando
```bash
sudo apt install ./webots_2023a_amd64.deb
```

Configurar webots para la compatibilidad con python.
Ejecutar los siguientes comandos
```bash
echo "export WEBOTS_HOME=/usr/local/webots" >> ~/.bashrc
```
```bash
echo "export PYTHONPATH=/usr/local/webots/lib/controller/python:$PYTHONPATH" >> ~/.bashrc

```



