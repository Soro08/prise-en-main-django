# prise-en-main-django

## Structure d'un projet Django

0. Initialisation
- Creation du dossier
- Creation de l'environnement virtuel : `python3 -m venv venv`
- Activation de l'environnement virtuel: `source venv/bin/activate`
- Deactiver l'environnement virtuel: `deactivate`
- Installation de Django: `pip install Django`

1. Création du projet Django
- Django admin startproject nom_du_projet
- Explication des fichiers

2. Configuration
- Création des dossiers
- Configuration dans le setings et dans l'url
````
# setings
    STATIC_URL = '/static/'
    STATIC_ROOT = BASE_DIR / 'static_cdn'
    MEDIA_URL = '/media/'
    MEDIA_ROOT = BASE_DIR / 'media_cdn'

    STATICFILES_DIRS = (BASE_DIR / 'static',)

#urls

from django.conf import settings
from django.conf.urls.static import static
..........

if settings.DEBUG:
    urlpatterns += static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
    urlpatterns += static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)

``` 
