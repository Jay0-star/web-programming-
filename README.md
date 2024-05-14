actually we are going to learn django very smoothly and it is mainly taught by our anish sir and the youtube channel named code aur chai

we have to understand that for the fast working we have to use uv here 
to make the virtual environment for django we have to type the python -m venv but if you have the package manager as uv then you have to type the uv venv

in the windows you have to type the .venv/scripts/activate

On the third day of the django development i just learn how to join render html 

from . import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.home, name="home"),
    path('about/',views.contact,name="contact")
]

by using above code we can just  put the path but the things is we have to write business logic in views which i mainly understand that it is the place where we can 
write code to show the templates or the response 

from django.http import HttpResponse ------------- it helps to get the httpresponse 
from django.shortcuts import render----------------- it helps to render the html file
def home(request):
    # return HttpResponse("you are at the position where you can learn anything faster than you think bro ")
    return render(request,'websites/index.html')
def about(request):
    return HttpResponse("you are at the position where you can learn anything faster than you think bro ")
def contact(request):
    return HttpResponse("we are from the place where you dont live that is dhapakhel and my contact num is 9808081238 ")
def jagsul(request):
    return HttpResponse("you are at the position where you can learn anything faster than you think bro ")



    to get the files from the templates we have to write the templates in dir of TEMPLATE which is in the setting
    to join the path of static and template first we have to import OS in the setting
    and then STATICFILES_DIRS = [os.path.join(BASE_DIR,'static')]

    and in the html file
    first we have to write {%load static%}

    in the href of link we have write {%static 'style.css'%}
