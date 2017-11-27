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

### 2.1. Utiliza los estilos en línea

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
