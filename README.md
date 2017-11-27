# Directrices de codificación de e-mails

Este documento ha sido creado para tratar de resolver dudas y problemas en referencia a la codificación de e-mails en HTML y CSS.


## Tabla de contenidos

1. [Introducción](#introduccion)
2. [Reglas básicas](#reglasbasicas)
3. [Enlaces de interés](#enlacesinteres)
4. [Contribuciones](#contribuciones)
5. [Copyright](#copyright)

<a name="introduccion"></a>
## 1. Introducción

Enviar un correo electrónico y que este se vea correctamente en todos los clientes de correo puede ser muy desesperante en algunas ocasiones.

Así pues, aquí trataré de dar algunos consejos y recopilar problemas, y sus respectivas soluciones, con los que muchos de nosotros nos hemos podido encontrar.


<a name="reglasbasicas"></a>
## 2. Reglas básicas

### 2.1. Utiliza estilos en línea

Algunos clientes de correo no leen corectamente los estilos si estos se aplican en el `head`, por lo que siempre es mejor poner los estilos en línea.

**Mal:**
```html
<head>
  .title {
    font-size: 16px;
    font-weight: bold;
  }
</head>
<body>
  <div class="title"></div>
</body>
```

**Bien:**
```html
<head></head>
<body>
  <div style="font-size: 16px; font-weight: bold;"></div>
</body>
```


### 2.2. Utiliza tablas y no bloques

A la hora de estructurar el contenido de un e-mail en columnas es importante **no utilizar `div` bajo ninguna circustancia, siempre utilizar `table`** en su lugar. 
De no hacerlo tendremos multitud de problemas con nuestra plantilla, sobretodo a la hora de restructurar el contenido según la resolución del dispositivo.

Además conviene añadir los valores cellpadding y cellspacing a 0. Esta es una buena forma de empezar una tabla:

```html
<table border="0" cellpadding="0" cellspacing="0">
  <tr>
    <td></td>
  </tr>
</table>
```

De la misma manera, también nos ayudará si todo el contenido de nuestra plantilla la ponemos dentro de una tabla ocupando todo el alto y ancho disponible, para así poder, por ejemplo, añadir un color de fondo. Aquí el código a usar:

```html
<table align="center" border="0" cellpadding="0" cellspacing="0" height="100%" width="100%">
  <tr>
    <td></td>
  </tr>
</table>
```


### 2.3. No excedas los 600px de ancho

Para asegurarnos de que nuestra plantilla se ve correctamente en todos los clientes de correo, nunca deberá superar los 600px de ancho.


### 2.4. Vigila con las imágenes

Todas las imágenes que contenga nuestra plantilla deberán tener la propiedad `style="display:block"`, para eliminar el espacio entre imágenes, y el atributo `alt`, para mostrar texto en aquellos clientes de correo que bloqueen las imágenes. 


### 2.5. No utilices JavaScript

Nunca nunca nunca añadas código JavaScript a un correo electrónico, no funcionará y además lo más probable es que sea vaya a la carpeta de *spam*.


<a name="enlacesinteres"></a>
## 3. Enlaces de interés

- [Guía de comptabilidades](https://www.campaignmonitor.com/css)


<a name="contribuciones"></a>
## 4. Contribuciones

Cualquier contribución es bienvenida, así que si tienes algo que ofrecer puedes hacerlo. Para aquellos que no sepáis como colaborar porque sois nuevos en GitHub comparto algunos enlaces que os serán de gran ayuda:

- [Cómo colaborar en un proyecto](https://gist.github.com/BCasal/026e4c7f5c71418485c1).
- [Sintaxis de los ficheros de texto](https://help.github.com/articles/basic-writing-and-formatting-syntax/).


<a name="copyright"></a>
## 5.Copyright

Copyright (c) 2017 [Aitor Rodríguez](http://www.frontendfactory.es). Licensed under the Apache License 2.0.
