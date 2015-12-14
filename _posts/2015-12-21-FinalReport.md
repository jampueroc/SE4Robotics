---
layout: post
title:  "Reporte final proyecto RQT-GraPharo"
date:   2015-11-17 09:00:00
author: Pablo - Jorge
categories: Reporte Final 
---
 
# Introducción
 
 En este reporte se muestran los avances logrados durante la iteración completa del proyecto.
 
# Problema y solución
 
 Es posible revisar el problema inicial y la solución propuesta para este en [Link Reporte Inicial](http://jampueroc.github.io/SE4Robotics/reporte/2015/09/26/Report) .
 
##Boton nodos /topicos.

Se creó estos botones para resolver el problema de los nodos/topicos en exceso ya que al hacerle click 
despliega los elementos correspondientes en una nueva ventana permitiendo seleccionar  un nodo/topico poder  esconderlo  o mostrarlo según se desee 
Al hacer esto se actualiza el grafo lo que permite visualizar especificamente lo que uno desea. Además es posible seleccionar 
mas de un elemento lo cual permite esconder grupos de manera fácil y rápida. 
Adicionalmente se agregó un campo de texto para realizar busquedas y facilitar la visualización.

##Grafo 

El grafo presenta varias funcionalidades extras:


1. Es posible seleccionar un nodo y moverlo dentro del area del grafo.
1. Se puede cambiar el tamaño del grafo.
1. Se puede hacer click en un nodo y se abrirá una ventana que mostrará el nombre del nodo con los publishers y subscribers.
1. Al hacer click en un tópico se puede ver el nombre del tópico y la información del último segundo que fue enviada a traves de él
1. Se agregó coloración a los nodo según la cantidad de publishers o subscribers (el usuario puede elegir y cambiar según desee).
1. Se agregó una leyenda explicativa sobres colores y elementos del grafo.
1. Se agregó un botón que permite esconder/visualizar nombres de nodos al hacer click.

#Limitaciones

1. Tiempo espera y uso de recursos para visualizar la última información publicada al hacer click en un tópico.
1. Falta implementar sistema configuración y manejo de información ya que se muestra la información del último minuto 
pero no se puede recargar la o cambiar el intervalo o la frecuencia que se obtienen los datos pero es facilmente extendible.
1. Flechas a sí mismo no se visualizan en el grafo aunque la información de la conexiones entre nodos este.
1. El Zoom presenta ciertas fallas ya que para que se actualice el grafo debe realizarse algún otro movimiento (click, mover grafo,etc)


