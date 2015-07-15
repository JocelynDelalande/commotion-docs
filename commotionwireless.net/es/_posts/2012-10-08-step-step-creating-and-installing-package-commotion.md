---
layout: blog
title: Paso a paso - creando e instalando un paquete para Commotion
categories: [chat,applications,routers,messaging]
created: 2012-10-08
changed: 2012-11-21
post_author: The Work Department
lang: es
---
  Aqu� en el Departamente de Trabajo, hemos estado ocupados creando sistemas para experimentar con aplicaciones que utilizan conexiones mesh de nodo a nodo y estamos ansiosos por compartirlas contigo. Particularmente, algunas de las aplicaciones ejemplo que proponemos en nuestro post <a class="external" href="https://commotionwireless.net/blog/exploring-meshaging" target="_blank"> Explorando el chat en las redes en malla &quot;Meshaging&quot;</a> que est�n tomando forma. Queremos ofrecerte las herramientas para experimentar lo que es posible dada la estructura arquitect�nica �nica de una red mesh. El software del router Commotion est� construido sobre OpenWRT, una distribuci�n Linux designada para routers y otros dispositivos peque�os. 
OpenWRT tiene un paquete de sistema de manejo, y el c�digo de Commotion est� guardado en un paquete y mecanismo de alimentaci�n separado. Un desarrollador puede integrar funciones adicionales en una red Commotion al escribir y portar aplicaciones y empaquetarlos para OpenWRT. A continuaci�n, se explica el proceso de portar y empaquetar una aplicaci�n (en este caso, un peque�o servidor websockets, ws-routing y dependencias).
<h3>Ingredientes</h3>Necesitar�s algunas cosas para continuar:
<ol><li>**�Una computadora! **Asumiendo que est�s usando una computadora en este momento, deber�a ser sencillo. Aseg�rate de tener algo de espacio en tu disco duro para descargar los paquetes.</li><li>**Acceso a la terminal y algunos comandos.** Necesitar�s estas herramientas, incluyendo <a class="external" href="http://git-scm.com/book/en/Getting-Started-Installing-Git" target="_blank">GIT</a> y <a href="http://www.gnu.org/software/make/manual/make.html#Top" target="_blank">Make</a>, para descargar y compilar el �ltimo c�digo de los repositorios.</li><li>**Wireless Router(s).** Este hardware es necesario para servir a tu red mesh. Puedes leer m�s detalles sobre el hardware que utilizamos aqu�: <a class="external" href="https://code.commotionwireless.net/projects/commotion-manual/wiki/Installing_Commotion_on_Wireless_Nodes#A-little-background" target="_blank">Instalando Commotion en Nodos Wireless</a>.</li><li>**Tiempo.** Como un buen platillo, algunos de estos scripts pueden tomar tiempo antes de estar listos. Se pueden anticipar, una o dos horas antes de que est� listo y en acci�n.</li><li>**Amigos.** No requeridos, pero aprender colaborativamente y trabajar juntos puede ser parte importante de la instalaci�n de las redes mesh.</li></ol><h3>
Paso a paso para para tener una delicia de red mesh</h3>Una vez que tengas lo esencial enumerado arriba, puedes comenzar a mezclarlo todo junto. 
En primer lugar, �vamos a construir los paquetes! Puedes hacer esto abriendo tu terminal e introduciendo los comandos que aparecen a continuaci�n en orden. Cualquier cosa despu�s de un signo de n�mero (#) est� ah� para proporcionar instrucciones adicionales y no se deber�a introducir a la l�nea de comandos. Los scripts de configuraci�n comandos de acciones pueden tomar tiempo para que corran, as� que ese ser�a un buen momento para leer el <a class="external" href="https://commotionwireless.net/blog" target="_blank">blog</a> o el <a class="external" href="https://commotionwireless.net/wiki/mesh-resources" target="_blank">Wiki de recursos de Mesh</a>.

	# Clona el commotion-openwrt repo:
	git clone https://github.com/opentechinstitute/commotion-openwrt.git
	cd commotion-openwrt
	./setup.sh
	cd ..
	# Clona tu paquete repo:
	git clone https://github.com/bnchdrff/commotion-wsrouting-feed.git commotion-examples
	# Corre el paquete setup.sh script:
	cd commotion-examples
	./setup.sh # ignore package feed errors
	# Configura y construye:
	cd ../commotion-openwrt/openwrt
	make menuconfig # ignore package feed errors
	# A ncurses GUI will display:
	## Selecciona el submenu commotion-apps 
	## Selecciona ws-routing as * (static) al presionar Y
	## Selecciona salir
	## Cuando se solicite, elige guardar config
	make V=99 # build, verbosely
	cd bin/ar71xx/
	ls

Y, �voil�! Deber�as ver una lista de archivos que se ven algo asi:
&quot;**openwrt-ar71xx-generic-ubnt-bullet-m-squashfs-factory.bin**&quot;. El archivo que necesitar�s mostrarle a tu router depender� del hardware del router. Usando ese archivo, sigue las instrucciones proporcionadas para <a class="external" href="https://code.commotionwireless.net/projects/commotion-manual/wiki/Installing_Commotion_on_Wireless_Nodes" target="_blank">Instalar Commotion en un nodo inal�mbrico</a> para actualizar el router. Estas <a class="external" href="https://code.commotionwireless.net/projects/commotion-manual/wiki/Detailed_TFTP_Instructions" target="_blank">instrucciones detalladas TFTP</a> tambi�n incluyen pasos para transferir el archivo a tu router con **TFTP.**
<h3>Ahora puedes probar Commotion</h3>�Bien hecho! Has instalado Commotion en tu router inal�mbrico. Despu�s que el router reinicie, puedes inhabilitar tu red conectada y brincar a la &ldquo;commotion_NNNNN_ap&rdquo; red que deber�a estar disponible. Abre un explorador web y navega a cualquier sitio, lo que deber�a llevarte a la p�gina splash de Commotion. Por �ltimo, puedes comprobar que el paquete **ws-routing** se haya instalado siguiendo estos pasos:
<ol><li>Clic &quot;**Ve a la configuraci�n de contrase�a...**&quot;</li><li>Haz clic en &quot;**Iniciar sesi�n**&quot; y resetea la contrase�a si es necesario.</li><li>El men� de administraci�n deber� aparecer arriba. Mueve el cursor sobre &quot;**Sistema**&quot; y da clic en &quot;**Software**.&quot; **ws-routing** deber�a estar en la lista.</li></ol>Aqu� una palmadita virtual en la espalda. Ahora estar�s listo para instalar aplicaciones ejemplo y probarlas t� mismo. En nuestro siguiente post, te mostraremos c�mo instalar y usar una aplicaci�n que hemos desarrollado.

