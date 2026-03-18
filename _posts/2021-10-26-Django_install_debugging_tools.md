---
author: Jihun Kim
categories:
- Software
- Django
comments: true
date: 2021-10-26 00:00:00 +0000
math: false
mermaid: false
pin: false
tags:
- Django
- Python
- Debug
- Setup
title: Django install Debugging Tools
---

---

# install

## pip

```bash
$ pip install django-debug-toolbar
```

## pipenv

```bash
$ pipenv shell
$ pipenv install django-debug-toolbar
```

# Setting

settings.py

```python
INSTALLED_APPS = [
	# ...
	'debug_toolbar',
	]

# ...

STATIC_URL = '/static/'

# ...

MIDDLEWARE = [
	# ...
	'debug_toolbar.middleware.DebugToolbarMiddleware',
	]

# ...

INTERNAL_IPS = [
	'127.0.0.1',
	]
```

urls.py

```python
from django.conf import settings
from django.URLS import path, include

# ...

if settings.DEBUG:
	import debug_toolbar
	urlpatterns += [
		path('__debug__/', include(debug_toolbar.urls))
	]
```