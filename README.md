﻿# django-likes
this is a app for django. It can liked or unliked something (comments, blog, and so on)

How to use:
1、Download and copy into you Django project.
2、Add this app into settings.py
   INSTALLED_APPS = [
    'likes',
    #others...
]

3、Add this app urls into project's urls
   urlpatterns = [
    url(r'^admin/', admin.site.urls),
    #open project's urls.py add this code
    url(r'^likes/', include('likes.urls')),
]

4、you can use it by ajax. request url link
   /likes/likes_change?type=blog&id=1&direct=1
   to add a likes in blog that blog id is 1.
   
   /likes/likes_change?type=blog&id=1&direct=-1
   to remove a likes
