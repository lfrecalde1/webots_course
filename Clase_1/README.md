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

## Configurar Bashrc
Configurar webots para la compatibilidad con python.
Ejecutar los siguientes comandos
```bash
echo "export WEBOTS_HOME=/usr/local/webots" >> ~/.bashrc
```
```bash
echo "export PYTHONPATH=/usr/local/webots/lib/controller/python:$PYTHONPATH" >> ~/.bashrc
```
```bash
source ~/.bashrc
```
## Installar Visual Studio Code

La forma mas sencilla de instalar Visual Studio Code es seguir los siguientes comandos para el terminal:
```bash
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
rm -f packages.microsoft.gpg
```

Actualizar el sistem e instalar Visual Studio Code
```bash
sudo apt install apt-transport-https
sudo apt update
sudo apt install code # or code-insiders
```
Ejecutar Visual Studio Code

```bash
code .
```

## Installar librerias python
Ejecutar los siguientes comandos en el terminal, los siguientes comandos instalar las librerias de numpy y scipy, las cuales son utilizadas para computo matricial
```bash
pip install numpy
pip install scipy==1.7.2
```





