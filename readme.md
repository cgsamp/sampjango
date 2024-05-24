# Sampjango

This is a sample project to exercise paketo buildpacks and the django framework

## Python

Install Python 
https://docs.python.org/release/3.11.7/


### venv

```bash
python -m venv venv
source venv/bin/activate
```

### pip

## Django

Create Django project

```
python -m pip install Django
django-admin startproject build
```

Create app within project

```
python manage.py startapp polls
```

## git


## Paketo

### Base

https://paketo.io/docs/howto/python/

Make sure it is a well formed Python project and that requirements.txt is present.

#### Buildpack.yaml


### Build

```
pack build polls --builder paketobuildpacks/builder-jammy-full
```

### Test

```
docker run --interactive --tty --publish 8000:8000 polls manage.py runserver 0.0.0.0:8000
```

From another terminal:
```
curl 127.0.0.1:8000/polls/ 
```

