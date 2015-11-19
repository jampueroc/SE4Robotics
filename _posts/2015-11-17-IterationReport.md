---
layout: post
title:  "Inicio proyecto RQT_GRAPH"
date:   2015-11-17 09:00:00
author: Pablo - Jorge
categories: Reporte Iteración 1 RQT-GraPharo
---
 
# Introducción
 
 En este reporte se muestran los avances logrados durante la primera iteración del proyecto.
 
# Problema y solución
 
 Es posible revisar el problema inicial y la solución propuesta para este en [Link Reporte Anterior](http://jampueroc.github.io/SE4Robotics/reporte/2015/09/26/Report) .
 
# Descripción del Trabajo realizado

## Primera Semana

Durante la primera semana se dedicó a realizar tutoriales de Pharo y Roassal para empezar a entender la funcionalidad del framework. De esta manera, se entenderían los elementos básicos para realizar el proyecto.

### Problemas encontrados

Lamentablemente la documentación se encuentra bastante desactualizada por lo que esto retrasó bastante la realización de los tutoriales.

### Logros Realizados Durante la Semana

Durante esta semana aunque no se realizó un avance en el código de la aplicación se logró entender como funciona Pharo y en ambiente de desarrollo de éste, ( como es la comunidad y documentación existente).

## Segunda Semana

La idea de esta semana era poder realizar el diseño básico de la interfaz (ventana, botones, menú, etc.) y sus funcionalidades mínimas pero, debido a la lógica de la linea de trabajo, se terminó realizando el trabajo correspondiente a la semana siguiente que correspondia a la creación del grafo de manera manual. Esto consiste en la creación del gráfico nodos-tópicos de manera autómatica, ingresando de los datos necesitados (nodos y tópicos). 


### Problemas encontrados

Durante esta semana se empezó trabajando usando `RTEdge` pero sus métodos estaban deprecados por lo que se buscó una clase para reemplazar y actualizar el código para ocuparla. Se encontró la clase `RTEdgeBuilder` que sus métodos estaban al día y se basan en la utilización de `RTEdge` para la creación de objetos gráficos.


### Logros Realizados Durante la Semana

Para esta semana se generó un grafo en el que es posible identificar, por color, a los nodos (según publicaciones y subscripciones), muestra sus nombres y los une según las conexiones existentes a través de algún tópico, graficándolo a través de una linea simple. Adicionalmente, se crearon dos test para probar las distintas conexiones. Uno consiste en la existencia de cuatro nodos donde hay: uno que no tiene tópicos, uno que se subscribe a un tópico, uno que publica y uno que publica y subscribe. De esta manera se prueba la identificación por color y las uniones simples. El otro test consiste en la unión de dos nodos a través de múltiples tópicos (vale decir, entre dos nodos, el inicial publica en más de un tópico y el final se subscribe en todos esos tópicos).



## Tercera Semana

Durante está semana se modificó el modelo que se había realizado la semana anterior y separó al objeto nodo del objeto tópico para poder agregarle información y funcionalidades extra, de manera que es posible observar la información de los tópicos y nodos de manera intuitiva. 

### Problemas encontrados
El modelo realizado anteriormente no resulto satisfactorio para el uso que se requeria para la aplicación porque no permitia diferencia varios tópicos que estuvieran asociados a dos nodos por lo que se debió pensar en un nuevo modelo en el cual los tópicos fueran un objeto con el atributo `onGraph` para poder diferenciar si dicho tópico habia sido agregado al grafo y que además pudiese almacenar información del tipo de mensaje que recibe y los datos que está publicando.

### Logros Realizados Durante la Semana

El grafo ahora muestra flechas como conexión entre nodos, además al hacer click muestra el nombre del tópico y logra diferenciar a varios tópicos que publican usando el mismo subscriptor y publicador. También es posible implementar la reacción de las flechas (tópicos) y nodos frente a las diferentes acciones del mouse sobre ellos. 

En la siguiente forma se muestra una imagen con el resultado obtenido en estas semanas.
![Grafo con varios tópicos]({{site.baseurl}}/assets/reports/022.png )


# Próximos avances

Debido a los cambios realizados en la semana 2 y 3, fue necesario actualizar el cronograma de trabajo (presente más abajo en el post). Esto se puede ver en [Cronograma Actualizado](http://jampueroc.github.io/SE4Robotics/cronograma/actualizado/2015/11/17/Cronograma) .


