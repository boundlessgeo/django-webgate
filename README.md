django-webgate
==============

A Django Authentication Middleware for WebGate Oracle Access Manager.

This is a subclass of the RemoteUserMiddleware. The header value is configurable by setting a django setting of WEBGATE_HEADER.

```python
WEBGATE_HEADER = 'HTTP_CUSTOM_WEBGATE_HEADER'
```
**Note:** The default header value is `HTTP_OAM_REMOTE_USER`

Quick Start
-----------

**1. Install using pip:**

```
pip install django-webgate
```

**2. Include "webgate" to your INSTALLED_APPS:**

```python
INSTALLED_APPS = [
    ...
    'webgate',
]
```
**3. Include "OracleAccessManagerMiddleware" in MIDDLEWARE_CLASSES:**

```python
MIDDLEWARE_CLASSES = (
    ...
    'webgate.middleware.OracleAccessManagerMiddleware',
)
```
