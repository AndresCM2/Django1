
# Crear proyecto

### Crear carpeta

Crear carpeta
```
mkdir PREMIOSPLATZI
```
Crear entorno virtual
```
py -m venv venv
```
Activar entorno virtual
```
.\venv\Scritps\activate
```
En caso de que estes en el bash de git el comando es
```
source venv/Scripts/activate
```
Instalar Django con el siguiente comando
```
pip install django
```
Validar la instalación de django
```
pip list
```
también podemos utilizar el siguiente comando
```
pip freeze
```
Para crear un archivo requirement escribir el siguiente comando
```
pip freeze > requirements.txt
```
Instalar un archivo desde requirement
```
pip install -r requirements.txt
```
