# Django - 104

## Requerimientos

* Complete las instrucciones previas [django-103](django-103.md)

## Instrucciones

* Desde la línea de comandos [LC], cree el super usuario administrador, con:

  ```
  python manage.py createsuperuser
  ```
  
  ❗**Nota:** Complete los datos (_username_, _email_ y _password_) solicitados para establecer las credenciales de acceso a la Administración de Django.

* [LC] Levante el servicio, con:

  ```
  python manage.py runserver
  ```
  
* Abra en el navegador el URL [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)
* Ingrese con las credenciales de acceso a la Administración de Django.

![Admin Site](https://docs.djangoproject.com/en/4.2/_images/admin02.png)

* Modifique el archivo `polls/admin.py` para habilitar el manejo de las operaciones **CRUD** de los modelos **Section** y **Product** desde la Administración de Django, con:

  ```
  from django.contrib import admin
  from .models import Section, Product

  admin.site.register(Section)
  admin.site.register(Product)
  ```
  
  ❗ **Nota:** Explore la **Administración de Django** para el manejo de las operaciones **CRUD** de los modelos **Section** y **Product**.
  
## Notas

Revise la documentación de la funcionalidad predeterminada de la [Administración de Django](https://docs.djangoproject.com/en/4.2/ref/contrib/admin/).

## Referencias

* Django. (2023). Retrieved 10 April 2023, from https://docs.djangoproject.com/en/4.2/intro/tutorial02/
* Django. (2023). Retrieved 11 April 2023, from https://docs.djangoproject.com/en/4.2/ref/contrib/admin/
