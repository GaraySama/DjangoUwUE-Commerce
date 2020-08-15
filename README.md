# UWU-commerce con DJANGO 9|B

Integrantes: Luis Orozco Jimenez, Jose Garay, Pedro de la Cruz, Tinoco Villarraeal

## Arrancar el proyecto

Primero te metes a la terminal de bash. Para instalar las dependencias y lo que se usara!

||||||||||||||||||||||
pip install virtualenv
||||||||||||||||||||||

Ejecutar este comando en caso de no tener la carpeta env

||||||||||||||
virtualenv env
||||||||||||||

Activamos la carpeta con el siguiente comando

|||||||||||||||||||||
source env/Scripts/active
|||||||||||||||||||||

Importante instalar las dependencias del proyecto...

||||||||||||||||||||||||||||||||
pip install -r instalaciones.txt
||||||||||||||||||||||||||||||||

Haces las migraciones

|||||||||||||||||||||||||||||||
python manage.py makemigrations
python manage.py migrate
||||||||||||||||||||||||||||||

Creas un superusuario para el Django admin
||||||||||||||||||||||||||||||||
python manage.py createsuperuser
||||||||||||||||||||||||||||||||||

Ya solo falta correr el servidor
||||||||||||||||||||||||||
python manage.py runserver
|||||||||||||||||||||||||||

**Note** Todo la instalacion de dependencias y creaciones se hacen en el bash

---

## Usage

The following routes for the api are:

### core/users

Esta ruta es para obtener todos los usuarios registrados en la API

### core/items/create

Esta ruta es para crear un nuevo articulo

||||||||||||||||||||||||||||||||||||||||
title = models.CharField(max_length=100)
price = models.FloatField()
discount_price = models.FloatField(blank=True, null=True)
category = models.CharField(choices=CATEGORY_CHOICES, max_length=2)
label = models.CharField(choices=LABEL_CHOICES, max_length=1)
slug = models.SlugField()
description = models.TextField()
image = models.ImageField()
||||||||||||||||||||||||||||||||||||||||||

### api/user/create

Esta ruta es para crear un usuario
||||||||||||||||||||||||||||||||||||||||
{
"name": "NAME",
"email": "EMAIL@DOMAIN.COM",
"password": "PASSWORD",
"password-again": "PASSWORD"
}

### api/orders

Aqui se hacen las ordenes por medio de la API
