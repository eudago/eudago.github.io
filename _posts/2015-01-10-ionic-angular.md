---
layout: post
title: Creando una aplicación con Ionic 2
description: "primer post sobre como crear una simple aplicación usando ionic 2 y angular 2."
modified: 2016-01-10
tags: [ionic,angular,javascript]
image:
  feature: post_ionic.png
  credit: eudago
---


### introducción

Aplicaciones nativas cada vez van a menos, por el simple echo que una aplicació hibrida escrita con javascript y html la puedes hacer correr en varios sistemas operativos a la vez y no tienes que precuparte, es decir pues crear una aplicación con Ionic 2 y Angular 2 tanto para ios como Android o una aplicación con electron y angular 2 y hacerla correr en os x, Linux y Windows.

A parte hay otras razones de peso para passarse a las aplicaciones hibridas, desde mi punto de vista hay una mejora substancial en quanto al aspecto visual de una aplicación y es que la cosa cambia mucho cuando tienes que utilizar Gtk o Cocoa vs (Html y css) las librerias nativas te són bastante restrictivas y es dificil salirse de los patrones, en cambio con html es mucho más facil crear.

### instalación

Primero de todo hay que instalar nodejs en nuestro equipo, a poder ser la ultima versión estable.

Luego passamos a instalar Ionic 2:

{% highlight html %}
npm install -g ionic@beta
{% endhighlight %} 
  
Tambien podemos aprovechar para instalar [ionic lab](http://lab.ionic.io/).
  
### creando el proyecto

Todo lo que haremos aquí podeis encontrar-lo en la propia web de Ionic 2

{% highlight html %}
ionic start nombre_proyecto --v2
cd nombre_proyecto
ionic serve
{% endhighlight %}

En caso de queos salga el error (como a mi) "cannot find module webpack" podeis solucionar-lo con:

{% highlight html %}
npm install webpack --save-dev --save-exact
{% endhighlight %}
    
al ejecutar la aplicación con ionic serve podremos ver que se nos abre una aplicación por defecto:

![app]({{ site.url }}/images/ionic1.png)

Bien esta es la aplicación por defecto de la que partiremos para crear una aplicación un poco mas compleja.


### aplicación

La aplicación trata de un pequeño juego tipo test, con una pregunta y cuatro opciones para responder y solo una valida, teniendo el jugador unas vidas determinadas y a cada fallo pierde una.

### estructura aplicacion ionic

Podemos ver que la estructura del proyecto tiene una pinta tal que:

![app]({{ site.url }}/images/ionicstructura.png)

Realmente para construir podemos obiar todas las carpetas y archivos y solo centrarnos en la estructura de app, que encontraremos dentro la carpeta app:

![app]({{ site.url }}/images/appstructure.png)

Cada componente estara formado por tres archivos, componente.js donde estara la logica del componente, componente.html y componente.scss donde se encontrara la parte visual del componente.

El componente principal es app.js,app.html que serà el primer componente que cargue al iniciar la apllicación.

Yo aparte del componente principal he creado dos componentes más info y game, el compoente info solo contiene información del juego y el componente game es el juego ensi.

Veamos la logica del juego game.js: 

<script src="https://gist.github.com/eudago/4e8d9b7bf4b6939ccfd5.js"></script>