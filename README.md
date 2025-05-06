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
    <title>POWER OF LAMP IN INCANDESCENT BULD</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <style type="text/css">
        body {
            background-color:white;
        }

        .edge {
            display: flex;
            height: 100vh;
            width: 100%;    
            justify-content: center;
            align-items: center;
        }

        .box {
            display: block;
            width: 500px;
            min-height: 300px;
            font-size: 20px;
            background: rgb(21, 208, 215);
            background: linear-gradient(90deg, rgb(99, 237, 118) 9%, rgb(193, 166, 202) 56%);
            border-radius: 10px;
            box-shadow: rgba(239, 5, 24, 0.35) 0px 5px 15px;
        }

        .formelt {
            color: whitesmoke;
            text-align: center;
            margin-top: 7px;
            margin-bottom: 6px;
        }

        h1 {
            color: white;
            text-align: center;
            padding-top: 20px;
        }
        input{
            margin: 5px;
            padding: 5px;
            border-radius: 5px;
            border: none;

        }
    </style>
</head>

<body>
    <div class="edge">
        <div class="box">
            <h1>POWER OF LAMP IN INCANDESCENT BULB</h1>
            <form method="POST">
                {% csrf_token %}
                <div class="formelt">
                    INTENSITY : <input type="text" name="Intensity" value="{{I}}"></input>(in A)<br />
                </div>
                <div class="formelt">
                    RESISITANCE : <input type="text" name="Resistence" value="{{R}}"></input>(in Ω)<br />
                </div>
                <div class="formelt">
                    <input type="submit" value="Calculate"></input><br />
                </div>
                <div class="formelt">
                    POWER : <input type="text" name="Power" value="{{Power}}"></input>W<br />
                </div>
            </form>
        </div>
    </div>
</body>

</html>
```

VIEWS.PY
```

```

URLS.PY

```

from django.contrib import admin
from django.urls import path
from side import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('PowerOfLampFilamentInAnIncandescentBulb/',views.powerlamp,name="PowerOfLampFilamentInAnIncandescentBulb"),
    path('',views.powerlamp,name="PowerOfLampFilamentInAnIncandescentBulb"),
]

```


## SERVER SIDE PROCESSING:

![Screenshot 2025-04-26 134248](https://github.com/user-attachments/assets/f537262c-0df4-4a13-88a9-556a1c000ba3)



## HOMEPAGE:
![Screenshot 2025-05-06 114305](https://github.com/user-attachments/assets/ddd3fa0b-35d7-4f8c-870f-4d5dafffaebf)



## RESULT:
The program for performing server side processing is completed successfully.
