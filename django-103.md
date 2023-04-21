# Django - 103

## Requerimientos

* Complete las instrucciones previas [django-102](django-102.md)
* Descargue e instale [PostgreSQL](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads).

## Instrucciones

* Configure la conexión con **PostgreSQL** en el archivo `project/settings.py`

    ```
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql_psycopg2',
            'NAME': 'postgres',
            'USER': 'postgres',
            'PASSWORD': '#Coloque aquí la contraseña#',
            'HOST': 'localhost',
            'PORT': '5432',
        }
    }
    ```

* Desde la línea de comandos [LC], migre los cambios en la base de datos, con:

  ```
  python manage.py migrate
  ```
  
* Revise los cambios en la base de datos.

* Agregue conexión con la aplicación **'api'** en el archivo `project/settings.py`
   
  ```
  INSTALLED_APPS = [
        'django.contrib.admin',
        'django.contrib.auth',
        'django.contrib.contenttypes',
        'django.contrib.sessions',
        'django.contrib.messages',
        'django.contrib.staticfiles',
        'api'
    ]
  ```

* Agregue los modelos **Section** y **Product** en `api/models.py`:

  ```
  from django.db import models
  
  class Section(models.Model):
    name = models.CharField(max_length=200)

  class Product(models.Model):
	section = models.ForeignKey(Section, on_delete=models.CASCADE)
	name = models.CharField(max_length=200)
  ```
  
  ❗**Nota**: La relación entre los modelos Section y Producto es de uno-a-muchos, mediante el atributo **section** en la clase Producto.

* [LC] Genere los archivos de migración de la aplicación **api**, con:

  ```
  python manage.py makemigrations api
  ```

* [LC] Migre los cambios en la base de datos, con:

  ```
  python manage.py migrate
  ```

* Revise los cambios en la base de datos.

### Opcional

Interactúe con el ORM desde la línea de comandos: 

* [LC] Active el shell de Python, con:
  
  ```
  python manage.py shell
  ```

* Explore el API de conexión con la base de datos, con:

  ```
  from api.models import Section
  
  s = Section(name="A1")
  
  s.save()
  ```

* Revise los cambios en la base de datos.

## Notas

* Revise la utilidad de las [aplicaciones](https://docs.djangoproject.com/en/4.2/ref/settings/#std-setting-INSTALLED_APPS) activas y el significado de una [migración](https://docs.djangoproject.com/en/4.2/ref/django-admin/#django-admin-migrate) en un proyecto de Django.

## Referencias

* Django. (2023). Retrieved 10 April 2023, from https://docs.djangoproject.com/en/4.2/intro/tutorial02/
