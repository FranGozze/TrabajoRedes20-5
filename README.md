[![Licencia](https://img.shields.io/github/license/FranGozze/TrabajoRedes20-5?color=purple)](https://github.com/FranGozze/TrabajoRedes20-5/blob/master/LICENSE)

# Mini internet :globe_with_meridians:
Este repositorio es un proyecto para la materia Conexión a Redes Extendidas (CRE) de 6to año informática del Instituto Politécnico Superior (IPS) de la Universidad Nacional de Rosario (UNR) 2020.
En el mismo se desarrolla un escenario que simula la red de un internet simplificado realizado con el entorno de trabajo kathara.

## Información básica :book:

### Escenario :mag:
El escenario sobre el cual trabajamos se encuentra en el archivo mini_internet.pdf de éste repositorio.<br>

### Requisitos y aplicaciones :floppy_disk:
A continuación se detallan las herramientas y aplicaciones necesarias para utilizar los archivos de éste repositorio en Linux.<br>
* Docker
* Kathara
* XTerm

Puede encontrar cómo instalar todo esto <a href="https://github.com/KatharaFramework/Kathara/wiki/Linux" target="_blank">aquí</a>.

### Documentación y uso :crossed_swords:
Algunos comandos utiles para utilizar el entorno kathara:<br>
* Levantar el laboratorio completo:
<pre><code>kathara lstart</pre></code>
* Detener el laboratorio completo:
<pre><code>kathara lclean</pre></code>
* Levantar una o más maquinas virtuales en el laboratorio:
<pre><code>kathara lstart &ltmv1&gt &ltmv2&gt &ltmv3&gt </pre></code>
* Detener una o más maquinas virtuales en el laboratorio:
<pre><code>kathara lclean &ltmv1&gt &ltmv2&gt &ltmv3&gt </pre></code>
* Levantar una o más maquinas virtuales:
<pre><code>kathara vstart &ltmv1&gt &ltmv2&gt &ltmv3&gt </pre></code>
* Detener una o más maquinas virtuales:
<pre><code>kathara vclean &ltmv1&gt &ltmv2&gt &ltmv3&gt </pre></code>
* Listar todas las maquinas virtuales activas:
<pre><code>sudo kathara list</pre></code>

## Licencia :scroll:
Éste repositorio está bajo la licencia GNU GPLv3.<br>
Para más información ver el archivo LICENSE.

## Comentarios :star:

### Integrantes del grupo
Franco Gozzerino<br>
Rosario Gonzales<br>
Ana Olivares<br>
Alan Hergenreder<br>

### Agradecimientos
A Alejandro Rodríguez Costello, profesor encargado de la asignatura.
