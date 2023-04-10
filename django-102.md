# Django - 102

## Requerimientos

* Complete las instrucciones previas [django-101](django-101.md)

## Instrucciones

* Desde la línea de comandos [LC], cree la aplicación **api**, con:

  ```
  python manage.py startapp api
  ```

* Agregue la vista _index_ en el archivo  `api/views.py`.

  ```
  from django.shortcuts import render
  from django.http import HttpResponse

  def index(request):
      return HttpResponse("Hola, mundo")
  ```

* Cree y modifique el archivo `api/urls.py` con los patrones de rutas y las vistas.

  ```
  from django.urls import path
  from . import views

  urlpatterns = [
      path("", views.index, name="index"),
  ]
  ```
  
* Modifique el archivo `project/urls.py` al agregar la referencia a la función **include** y los patrones de rutas de la aplicación `api/urls.py`.

  ```
  from django.contrib import admin
  from django.urls import include, path

  urlpatterns = [
      path("api/", include("api.urls")),
      path('admin/', admin.site.urls),
  ]
  ```

* [LC] Levante el servicio, con:

  ```
  python manage.py runserver
  ```
  
* Abra en el navegador el URL [http://127.0.0.1:8000/api/](http://127.0.0.1:8000/api/)

## Notas

* Revise en la [documentación de Django](https://docs.djangoproject.com/en/4.1/intro/tutorial01/) la diferencia entre **proyecto y aplicación**, la estructura de archivos de una aplicación y la función **include()**.

## Referencias

* Django. (2023). Retrieved 10 April 2023, from https://docs.djangoproject.com/en/4.2/intro/tutorial01/#creating-the-polls-app
