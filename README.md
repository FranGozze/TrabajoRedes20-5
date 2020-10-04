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

## Informacion avanzada :books:

### Configuracion de routers y servidores :satellite:
Utilizamos los protocolos correspondientes al archivo adjunto en el repositorio para configurar cada zona del escenario.
Además, realizamos los dominios y la construcción de los servidores en base a los ejercicios subidos a la plataforma donde se desarrollo el curso de la materia.<br>

#### Demonios :space_invader: 

Para activar los demonios requeridos primero editamos el archivo <code>daemons</code> que se encuentra en: <code>/etc/quagga/daemons</code><br>
y por defecto luce así.
<pre><code>zebra=no
bgpd=no
ospfd=no
ospf6d=no
ripd=no
ripngd=no</pre></code>

Tras cambiar cualquier <code>no</code> por <code>yes</code>, se activara el demonio, que puede ser configurado individualmente en cada router con un archivo <code>~.conf</code> correspondiente localizado en <code>/etc/quagga/</code><br>
Los demonios utilzados en este escenario fueron:
* Zebra
* OSPDF
* RIPD

Puede encontrar más informacion de protocolos <a href="https://www.halolinux.us/networking/using-zebra.html" target="_blank">aquí</a> y también por <a href="https://sites.google.com/site/tuxnots/materias-de-la-facu/gnu-linux/proyectozebraquaggaconfiguraciones" target="_blank">aquí</a>.

#### Comandos más usados :recycle:

* <code>redistribute connected</code><br>
Comparte las tablas de routeo a todos los demás routers.

* <code>stub</code><br>
Genera una sub-area dentro de un rango de red para administrar la zona por partes.

* <code>ifconfig</code><br>
Levanta la conexion de dicha maquina con un cable en un puerto

* <code>route add</code><br>
Agrega un router a la tabla con un puerto y un flag.

* <code>network</code><br>
Agrega un area de la red a la tabla de ser posible.

* <code>ping</code><br>
Envia un mensaje para verificar la conexion entre dos maquinas (muy utlizado para testear).

* <code>traceroute</code><br>
Lo mismo que ping pero marcando la ruta del mensaje.

* <code>dig</code><br>
Verifica la asignacion de un dominio sobre los servidores. 

* <code>links</code><br>
Conecta a un dominio para testear el host de un servidor.

#### Apache y Nginx :mailbox_with_mail:
Los servidores se activan de forma similar con el comando <code>start</code> en los archivos <code>~.startup</code> de cada servidor, y luego se configuran con sus respectivas carpetas en <code>/etc/apache2/...</code> o bien <code>/etc/nginx/...</code> según el caso.

Ejemplos:
<pre><code>/etc/init.d/nginx start</pre></code>
<pre><code>/etc/init.d/apache2 start</pre></code>

Cabe aclarar que para trabajar con Nginx sobre kathara hay que modficar la imagen de Docker, puesto que Nginx no está incluido por default.

Puede encontrar más información de Nginx <a href="http://wiki.nginx.org/ImapAuthenticateWithApachePhpScript" target="_blank">aquí</a>.<br>
Puede encontrar más información de Apache <a href="https://httpd.apache.org/docs/2.4/configuring.html" target="_blank">aquí</a>.


## Licencia :scroll:
Este repositorio está bajo la licencia GNU GPLv3.<br>
Para más información ver el archivo LICENSE.

## Comentarios :star:

### Integrantes del grupo
Franco Gozzerino<br>
Rosario Gonzales<br>
Ana Olivares<br>
Alan Hergenreder<br>

### Agradecimientos
A Alejandro Rodríguez Costello, profesor encargado de la asignatura.
