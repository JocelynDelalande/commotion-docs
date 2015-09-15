---
layout: blog
title: Lanzamiento del test MeshTether 
categories: []
created: 2012-08-23
changed: 2013-07-26
post_author: Hans-Christoph Steiner
lang: es
---
  Commotion MeshTether es una aplicaci�n Android que tiene por objetivo conectarse con los OLSR meshes con un simple clic. Viene configurado por default en el Commotion mesh, pero puede ser configurado por completo, y puede tener m�ltiples &quot;perfiles&quot; para elegir.
Estas son dos pesta�as: Links e Info. Links muestra todos los links 
first-hop e Info muestra todos los ajustes wifi config y olsrd.conf. 
Adicionalmente, puedes compartir/enviar por correo informaci�n depurada de la app del men�.
Est� trabajando bastante bien en el Nexus One I&#39;m usado para pruebas. Yo tambi�n he probado el HTC Wildfire, Motorola Droid, y HTC myTouch 3G.
Los perfiles mesh se implementan as�:
<ul><li>(default) usa los ajustes wifi/ip de las preferencias y la olsrd.conf que se incluye en la app</li><li>el resto se escanea del sistema de archivos en dos lugares:<ul><li>en el folder de la app app_bin/ folder</li><li>/mnt/sdcard/MeshTether (por ejemplo, el folder MeshTether en la tarjeta SD)</li></ul></li><li>el esc�ner busca en estos folders por *.propiedades de archivos y toma el nombre del archivo como su nombre de perfil (por ejemplo,  myprofile.properties ser� ligado a la secci�n  &quot;myprofile&quot; del men� de perfiles)</li><li>si hay una myprofile.conf seguida de myprofile.properties entonces lo usar� como la olsrd.conf. de otro modo, utilizar� la olsrd.conf incluida</li><li>las opciones de propiedades son:<br />ssid=commotionwireless.net<br />bssid=02:CA:FF:EE:BA:BE<br />channel=5<br />ip=172.29.0.0<br />ipgenerate=true<br />netmask=255.255.0.0<br />dns=8.8.8.8</li><li>todas se requieren, a excepci�n de &#39;ipgenerate&#39;, que marca la &#39;ip&#39; como la ra�z para la generaci�n del algoritmo IP. Si &#39;ipgenerate&#39; est� desactivada o no es &#39;true&#39;, entonces la &#39;ip&#39; se usa tal cual.</li></ul>Aqu� hay un test apk:
<a href="https://guardianproject.info/builds/CommotionMeshTether/2012-08-22/" target="_blank">https://guardianproject.info/builds/CommotionMeshTether/2012-08-22/</a><br />md5: 176008560f00d8cef65f0e3e781884e1<br />sha1: b9151fb635185880007411fd49e8ab5b254ad750
�Int�ntalo y dinos c�mo te funcion�!


