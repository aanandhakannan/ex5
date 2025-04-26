# Ex.05 Design a Website for Server Side Processing
## Date: 26-04-2025

NAME : AANANDHA KANNAN S 

REG NO : 212224040003

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<html>
<head>
<meta charset='utf-8'>
<meta http-equiv='X-UA-Compatible' content='IE=edge'>
<title>Surface Area of Right Cylinder</title>
<title>AANANDHA KANNAN S (212224040003)</title>
<meta name='viewport' content='width=device-width, initial-scale=1'>
<style type="text/css">
body
{
background-color:rgb(11, 210, 228);
}
.edge {
width: 1440px;
margin-left: auto;
margin-right: auto;
padding-top: 250px;
padding-left: 300px;
}
.box {
display:block;
border: Thick dashed rgb(8, 6, 17);
width: 500px;
min-height: 300px;
font-size: 20px;
background-color:rgb(209, 20, 42);
}
.formelt{
color:rgw(1, 18, 17);
text-align: center;
margin-top: 7px;
margin-bottom: 6px;
}
h1
{
color:rgb(17, 232, 239);
text-align: center;
padding-top: 20px;
}
</style>
</head>
<body>
<div class="edge">
<div class="box">
 AANANDHA KANNAN S (212224040003)
<h1>Surface Area of Right Cylinder</h1>
<form method="POST">
{% csrf_token %}
<div class="formelt">
Radius : <input type="text" name="radius" value="{{r}}"></input>(in m)<br/>
</div>
<div class="formelt">
Height : <input type="text" name="height" value="{{h}}"></input>(in m)<br/>
</div>
<div class="formelt">
<input type="submit" value="Calculate"></input><br/>
</div>
<div class="formelt">
Area : <input type="text" name="area" value="{{area}}"></input>m<sup>2</sup><br/>
</div>
</form>
</div>
</div>
</body>
</html>
```

VIEWS.PY
```
from django.shortcuts import render
def surfacearea(request):
    context={}
    context['area'] = "0"
    context['r'] = "0"
    context['h'] = "0"
    if request.method == 'POST':
        print("POST method is used")
        r = request.POST.get('radius','0')
        h = request.POST.get('height','0')
        print('request=',request)
        print('radius=',r)
        print('height=',h)
        area = 2 * 3.14 * int(r) * int(h) + 2 * 3.14 * int(r) * int(r)
        context['area'] = area
        context['r'] = r
        context['h'] = h
        print('Area=',area)
    return render(request,'mathapp/math.html',context)
```

URLS.PY

```
from django.contrib import admin
from django.urls import path
from mathapp import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('surfaceareaofcylinder/',views.surfacearea,name="surfaceareaofcylinder"),
    path('',views.surfacearea,name="surfaceareaofcylinderroot")
]

```


## SERVER SIDE PROCESSING:

![Screenshot 2025-04-26 134248](https://github.com/user-attachments/assets/f537262c-0df4-4a13-88a9-556a1c000ba3)



## HOMEPAGE:

![Screenshot 2025-04-26 134103](https://github.com/user-attachments/assets/244dab61-c6c0-4cd5-955a-f59724e381d1)


## RESULT:
The program for performing server side processing is completed successfully.
