# Django - 101

## Requerimientos

Desde la línea de comandos, instalar **Psycopg2** (Interfaz para trabajar con PostgreSQL) y **Django**:

```
python -m pip install psycopg2-binary django
```

## Instrucciones

* Crear un proyecto plantilla, con: 
  
  ```
  python -m django startproject project
  ```

* Acceda a la carpeta del proyecto, con:

  ```
  cd project 
  ```

* Levante el servicio, con:

  ```
  python manage.py runserver
  ```

## Notas

Revise en la [documentación de Django](https://docs.djangoproject.com/en/4.1/intro/tutorial01/) el uso de los archivos **manage.py**, **settings.py**, y **models.py** en un proyecto de Django.

## Referencias

[1] Django. (2023). Retrieved 5 April 2023, from https://docs.djangoproject.com/en/4.1/intro/tutorial01/
