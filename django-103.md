# Django - 102

## Requerimientos

* Complete las instrucciones previas [django-101](django-101.md)
* Descargue e instale [PostgreSQL](https://www.enterprisedb.com/downloads/postgres-postgresql-downloads).

## Instrucciones

* Cree la aplicación **orm**, con:

```
python manage.py startapp orm
```

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

## Notas

* Revise en la [documentación de Django](https://docs.djangoproject.com/en/4.1/intro/tutorial01/) la diferencia entre **proyecto y aplicación**.

## Referencias

* Django. (2023). Retrieved 10 April 2023, from https://docs.djangoproject.com/en/4.2/intro/tutorial01/#creating-the-polls-app
