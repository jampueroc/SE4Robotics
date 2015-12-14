---
layout: post
title:  "Reporte final proyecto RQT-GraPharo"
date:   2015-11-17 09:00:00
author: Pablo - Jorge
categories: Reporte Final 
---
 
# Introducción
 
 En este reporte se muestran los avances logrados durante la iteración completa del proyecto. Se pretende ilustrar al lector
 respecto a las distintas funcionalidades creadas durante el periodo del proyecto.
 
# Problema y solución
 
 Es posible revisar el problema inicial y la solución propuesta para este en [Link Reporte Inicial](http://jampueroc.github.io/SE4Robotics/reporte/2015/09/26/Report) .
 
# Aplicación realizada
 
 A continuación se describirán los distintos elementos que posee la aplicación
 
## Botón nodos /tópicos.

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/032.png" width="500">

Se crearon estos botones para resolver el problema de los nodos/tópicos en exceso. Al hacer click sobre estos se
despliegan los elementos correspondientes en una nueva ventana que permite seleccionar uno o varios nodos/tópicos y ocultarlos o mostrarlo según se desee.

Adicionalmente se agregó un campo de texto para realizar búsquedas en la lista de nodos/tópicos y facilitar la visualización de la lista.

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/036.png" width="300">

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/037.png" width="500">

Al hacer esto la gráfica se actualiza, permitiendo visualizar específicamente lo que el usuario quiere ver.

## Botón refresh

Este botón permite realizar la actualización de los elementos del grafo sin tener la necesidad de cerrar y volver a abrir la aplicación. Además actualiza la información de nodos y tópicos desde ROS.


## Gráfico

El gráfico presenta varias funcionalidades extras:

* Es posible seleccionar un nodo y moverlo dentro del área del grafo.
* Se puede cambiar el tamaño del grafo.
* Se puede hacer click en un nodo y se abrirá una ventana que mostrará el nombre del nodo con los publishers y subscribers.

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/031.png" width="500">


* Al hacer click en un tópico se puede ver el nombre del tópico y la información del último segundo que fue enviada a través de él.

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/039.png" width="500">


* Se agregó coloración a los nodos según la cantidad de publishers o subscribers (el usuario puede elegir y cambiar según desee).
* Se agregó una leyenda explicativa sobres colores y elementos del grafo.
* Se agregó un sistema de selección que permite esconder/visualizar nombres de nodos al hacer click.

<img src="https://raw.githubusercontent.com/jampueroc/SE4Robotics/gh-pages/assets/reports/045.png" width="500">

#Limitaciones

1. El tiempo de espera y uso de recursos para visualizar la última información publicada al hacer click en un tópico es superior a lo que debería ser.
1. Falta implementar un sistema de configuración y manejo de información en los tópicos. Actualmente muestra la información del último minuto, sin posibilidades de recargar la información o cambiar los parámetros (intervalo, frecuencia, entre otros) ante los cuales se obtienen los datos.
1. Los nodos que publican sobre el mismo tópico al cual están subscriscritos no se visualizan en el grafo, aunque la información de la conexiones entre nodos existe.
1. El Zoom presenta ciertas fallas ya que para que se actualice el grafo debe realizarse algún otro movimiento (click, mover grafo,etc).


