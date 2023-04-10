# Django - 102

## Requerimientos

* Complete las instrucciones previas [django-101](django-101.md)

## Instrucciones

* Cree la aplicación **api**, con:

  ```
  python manage.py startapp api
  ```

* Agregue la vista _index_ en el archivo  `api/views.py`

  ```
  from django.shortcuts import render
  from django.http import HttpResponse

  def index(request):
      return HttpResponse("Hola, mundo")
  ```

* Cree el archivo `api/urls.py`

* Agregue la ruta raíz (`'/'`) en el archivo `api/urls.py`

  ```
  from django.urls import path
  from . import views

  urlpatterns = [
      path("", views.index, name="index"),
  ]
  ```

* Levante el servicio, con:

  ```
  python manage.py runserver
  ```

## Notas

* Revise en la [documentación de Django](https://docs.djangoproject.com/en/4.1/intro/tutorial01/) la diferencia entre **proyecto y aplicación** y la estructura de archivos de una aplicación.

## Referencias

* Django. (2023). Retrieved 10 April 2023, from https://docs.djangoproject.com/en/4.2/intro/tutorial01/#creating-the-polls-app
