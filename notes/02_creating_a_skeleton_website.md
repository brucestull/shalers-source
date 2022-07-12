# Django Tutorial Part 2: Creating a skeleton website
* https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/skeleton_website

## Process:
1. Create the `catalog` app:  
    * `python manage.py startapp catalog`
    ```
    C:\USERS\BRUCE\PROGRAMMING\SHALERS-SOURCE\CATALOG
    |   admin.py
    |   apps.py
    |   models.py
    |   tests.py
    |   views.py
    |   __init__.py
    |
    \---migrations
            __init__.py
    ```

1. SIDE NOTE: Added `app_name` to `users\urls.py`.

1. Add following to `library_project\urls.py`:  
	```
	urlpatterns = [
	...
	path('catalog/', include('catalog.urls')),
	]
	```

1. Create `catalog\urls.py` and add content:  
	```
	from django.urls import path, include
	from . import views

	app_name = 'catalog'
	urlpatterns = [
		
	]
	```

1. Test server and expect error since we don't have `catalog/urls.py` set up yet:  
	```
	Page not found (404)
	Request Method:	GET
	Request URL:	http://localhost:8000/catalog/
	Using the URLconf defined in library_project.urls, Django tried these URL patterns, in this order:

	[name='home']
	admin/doc/
	admin/
	users/
	users/
	The current path, catalog/, didn’t match any of these.

	You’re seeing this error because you have DEBUG = True in your Django settings file. Change that to False, and Django will display a standard 404 page.
	```



