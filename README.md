# django-skeleton
> Configuracion incial de Django
```
1.- Al clonar el repositorio, se debe de crear el entorno virtual
    $ git clone git@github.com:Alhexander/django-skeleton.git
    $ cd django-skeleton/
    $ virtualenv -p python3 .venv
    $ source .venv/bin/active ("Nota: para linux")
    $ pip install django==2.2.7
    $ django-admin startproject "NOMBRE_PROJECT" . 
    $ pip install psycopg2-binary psycopg2 ("Nota: Configuracion de postgres")
    
```
> Configuracion de setting.py, para postgres:

```python
# Database
# https://docs.djangoproject.com/en/2.2/ref/settings/#databases

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}

# Se realizara este cambio para utilizar Postgresql

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'NOMBRE_DB',
        'USER': 'NOMBRE_USUARIO',
        'PASSWORD': 'CONTRASEÑA',
        'HOST': '127.0.0.1',
        'PORT': '5432',
        }
}

```
    $ pip freeze > requirements.txt 
```
