# Creacion de primer Aplicación

1. ### ***Ejecutar el siguiente comando para crear la primera aplicación***

```
python manage.py startapp polls
```
2. ### ***Crear mi primer hola mundo***

En el archivo de la ruta `polls|views` incluir el siguiente código.

```py
from django.shortcuts import render
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello world")
```
Para conectar este mensaje tenemos que crear una conexión incluyendo la ruta en la en el archivo de las urls `premiosplatziapp|urls.py`.

```py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('polls/',include('polls.urls'))
```
Para conectar esta nueva inclusión de url se requiere crear un archivo con el nombre `urls.py` en en la ruta `polls|urls.py`.
```
touch urls.py
```
Ingresar el siguiente código en esta ruta.

```py
from django.urls import path
#--------------------------------
from . import views

urlpatterns=[
    path('',views.index,name='index')
```
Se nos dirigimos al localhost de la ruta `/polls` aparecerá el mensaje de hola mundo.   
<p align="center">

<img src="https://drive.google.com/uc?export=download&id=1U8ObzPFQXSGhBSNSWjGFqdXpoov5PyGE" width="500" height="500" />

</p>

