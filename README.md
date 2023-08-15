# django-docker

## build and django startproject

```bash
docker-compose run web django-admin startproject composeexample .
```

## django database setting

edit composeexample/settings.py DATABASE

```PYTHON
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'django',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'db',
        'PORT': 3306,
    }
}
```

### docker-compose up

```bash
docker-compose up
```

### django database migrate and create superuser

```bash
docker-compose exec web bash
```

django database migration

```bash
python manage.py migrate
```

django create superuser

```
python manage.py createsuperuser
```

### Login

[`localhost:8000/admin`](http://localhost:8000/admin/)