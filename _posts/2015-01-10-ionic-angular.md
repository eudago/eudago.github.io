---
layout: post
title: Creando una aplicación con Ionic y Angular 2
description: "primer post sobre como crear una simple aplicación usando ionic 2 y angular 2."
modified: 2016-01-10
tags: [ionic,angular,javascript]
image:
  feature: post_ionic.png
  credit: eudago
---


### introducción

Aplicaciones nativas cada vez van a menos, por el simple echo que una aplicació hibrida escrita con javascript y html la puedes hacer correr en varios sistemas operativos a la vez y no tienes que precuparte, es decir pues crear una aplicación con Ionic 2 y Angular 2 tanto para ios como Android o una aplicación con electron y angular 2 y hacerla correr en os x, Linux y Windows.

A parte hay otraz razones de peso para passarse a las aplicaciones hibridas, desde mi punto de vista hay una mejora substancial en quanto al aspecto visual de una aplicación y es que la cosa cambia mucho quando tienes que utilizar Gtk o Cocoa vs (Html y css) las librerias nativas te són bastante restrictivas y es dificil salirse de los patrones, en cambio con html es mucho más facil crear.

### instalación

Primero de todo hay que instalar nodejs en nuestro equipo, a poder ser la ultima versión.

Luego passamos a instalar Ionic 2:

    npm install -g ionic@beta
    
### creando el proyecto

Todo lo que haremos aquí podeis encontrar-lo en la propia web de Ionic 2

    ionic start nombre_proyecto --v2
    cd nombre_proyecto
    ionic serve
    
En caso de queos salga el error (como a mi) "cannot find module webpack" podeis solucionar-lo con:

{% highlight html %}
    npm install webpack --save-dev --save-exact
{% endhighlight %}
    
al ejecutar la aplicación con ionic serve podremos ver que se nos abre una aplicación por defecto:

![app]({{ site.url }}/images/ionic1.png)

Bien esta es la aplicación por defecto de la que partiremos para crear una aplicación un poco mas compleja.

### aplicación

