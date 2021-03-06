---
layout: blog
title: Desarrollo de etiqueta de advertencia, Parte 1
categories: [es]
tags: [warning,label,security,anonymity,privacy,Research]
created: 2013-02-25
changed: 2013-07-26
post_author: OTI
lang: es
---
  Commotion es actualmente una herramienta segura de evasión. 

En algún punto esa declaración no será verdad, pero hasta entonces este hecho debe ser conocido por cualquier persona que interactúa con Commotion. Con la creciente popularidad de las herramientas digitales de evasión, medios de prensa han señalado a Commotion como una posible herramienta para la creación de redes de comunicación locales seguras cuando los canales habituales se ven comprometidos. Cuando un proyecto inacabado como Commotion entra en el centro de atención, es importante advertir a los usuarios potenciales sobre las limitaciones de las herramientas de desarrollo. En las comunidades de evasión y criptografía, esto se suele hacer con una advertencia. Este post recorrerá nuestro proceso de desarrollo de una etiqueta de advertencia. Esperamos que ayude a los nuevos proyectos que se enfrentan a este mismo dilema.
Decidimos enmarcar nuestra búsqueda de una advertencia haciendo dos preguntas. ¿Qué información es importante para que un usuario potencial de Commotion tome una decisión informada? ¿Cómo aseguramos la &quot;habilidad del individuo leyendo \[la advertencia\] para entender la información para tomar la acción deseada&quot;\[1\] para su situación específica?
Hicimos una lluvia de ideas de advertencias específicas de países que identifican amenazas locales de guardianes de los derechos de Internet\[2\] para crear advertencias personalizables para distintos niveles de amenazas. Pero con herramientas de anonimato de ubicaciones\[3\] y variantes individuales de amenazas, decidimos crear una advertencia unificada que se enfocara en lo que Commotion no puede hacer. En términos generales, Commotion es un juego de herramientas que permite a los routers inalámbricos, laptos y computadoras de escritorio, teléfonos android enrutados, y estaciones base de teléfonos celulares de softwares definidos encontrarse y comunicarse con y a través de, el uno con el otro. Qué es lo que Commotion es incapaz de hacer es una pregunta difícil. Commotion es incapaz de hacer muchas cosas. No puede andar en bicicleta o contabilizar mis impuestos. Pero, la mayoría de los usuarios no esperan estas cosas. Con el fin de indicar a los usuarios potenciales lo que Commotion no puede hacer, necesitábamos averiguar el conjunto potencial de la funcionalidad que los usuarios esperan de Commotion. Para descubrir las expectativas posibles, escaneamos nuestro propio alcance y la prensa que hemos recibido para ver lo que transmitió a los que lo leen. Aquí está una colección de los fragmentos más destacados, y qué funcionalidad se extrae de ellos.
Red inalámbrica segura independiente para conflictos y desastres:
<blockquote>&quot;\[El\] Internet en una maleta (Internet in a Suitcase) es básicamente un programa de software destinado a dar a las personas en zonas de conflicto o desastres la capacidad de establecer una red inalámbrica segura e independiente sobre sus computadoras y teléfonos celulares.&quot; \[4\]</blockquote> 
Dispositivos y herramientas de infraestructura independiente centralizada que eliminan la vigilancia y el monitoreo mientras que garantizan la identidad de las personas al comunicarse:
<blockquote>&quot;Esta es una red completamente ad hoc, no hay dependencia de ningún dispositivo a cualquier otro dispositivo y elimina un punto central para el comando y vigilancia de control y monitoreo,&quot; dijo Meinrath. &quot;Nosotros también disponemos de autentificación entre cada salto en la red y el cifrado a través de cada salto.&quot; \[4\]</blockquote> 
Llamadas telefónicas gratuitas:
<blockquote>&quot;La estupenda aplicación de la que hablé con mucha gente, es que, si tienes un sistema como este, no hay razón por la que necesites pagar por una llamada local de nuevo&quot; una vez que hayas descargado el software que le permita a tu dispositivo unirse a la red wifi, &quot;porque simplemente estás comprobando la disponibilidad de máquina a máquina de una red local,&quot; dijo Meinrath. \[4\]</blockquote> 
Tecnología barata para routers y teléfonos Android para disidentes para evadir la censura:
<blockquote>&quot;Él y un equipo de ingenieros de software están desarrollando software de código abierto para convertir puntos de acceso inalámbrico baratos y teléfonos inteligentes Android en nodos de red, que luego podrían ser utilizados por los disidentes para evadir la censura y difundir las conexiones de bajo costo en todas partes del mundo.&quot; \[6\]</blockquote> 
Fácil de instalar y configurar:
<blockquote>&rdquo;El firmware provee capacidades de auto-configuración,&rdquo; dijo Brian Duggan, uno de los ingenieros del proyecto Internet in a Suitcase, &ldquo;así que no necesitas ser un ingeniero&rdquo; para instalarlo. &ldquo;Puedes incluir tantos nodos como quieras, o puedes recoger los anteriores.&rdquo; \[6\]</blockquote> 
Acceso a Internet tolerante a los retrasos:
<blockquote>&ldquo;Podrías tener un Twitter tolerante a retrasos, donde la gente en la red local pudiera ver tus tweets y luego, cuando la conexión se restaure pudieran ser publicados al Internet,&rdquo; Meinrath dijo. &ldquo;Estamos en la infancia de este tipo de intranet.&rdquo; \[6\]</blockquote> 
Somos rockstars (totalmente cierto):
<blockquote>&quot;Una operación salida de una novela de espías en el quinto piso de una tienda en la calle L en Washington, donde un grupo de jóvenes emprendedores que parecen como si estuvieran en una banda de garage, están adecuando hardware que parece engañosamente inofensivo en un prototipo de &ldquo;Internet en una maleta.&rdquo; \[5\]</blockquote> 
Separado de la infraestructura independiente, imposible de apagar, controlar o vigilar:
<blockquote>&ldquo;Vamos a construir una infraestructura separada donde la tecnología sea casi imposible de apagar, controlar o vigilar.&rdquo; \[5\]</blockquote> 
Red descentralizada usando teléfonos, computadoras:
<blockquote>&quot;Commotion es una herramienta de comunicación de código abierto que usa teléfonos móviles, computadoras y otros dispositivos inalámbricos para crear redes mesh descentralizadas.&quot; \[7\]</blockquote> 
Comparte el Internet:
<blockquote>&quot;El software de Commotion también permite a los usuarios en una red mesh compartir el acceso al Internet. El software no proporciona acceso a Internet, pero sí permite que varios dispositivos compartan sus conexiones.&quot; \[7\]</blockquote> 
Red robusta que garantiza el anonimato y evade la censura, incluso cuando otros sistemas de comunicación han fracasado:
<blockquote>&quot;Commotion es un set flexible de herramientas que pueden funcionar bien en diferentes escenarios. 
Pueden crecer, encogerse, y moverse según sea necesario y de acuerdo con los recursos disponibles. Commotion está organizado y mantenido por miembros de la comunidad para satisfacer sus necesidades. Puede actuar como una red troncal para la infraestructura de last-mile, una red local comunitaria, un canal de comunicación de elusión y anonimato protegido, o una infraestructura de comunicaciones de emergencia local cuando se cortan los sistemas existentes.&quot; \[7\]</blockquote> 
Esta serie de citas nos dieron una idea de lo que habíamos presentado como estados actuales y futuros de Commotion, y entonces, lo que le esperaba a los usuarios Commotion cuando vayan a descargarlo. Tomamos estas notas y las compilamos en una lista de lo que el actual lanzamiento de Commotion todavía NO puede hacer.
Commotion no:
<ul><li>Provee anonimato</li><li>Provee comunicación con tolerancia a los retrasos</li><li>Previene el monitoreo de tu uso del Internet</li><li>Te permite llamar a otros teléfonos que no estén habilitados con Commotion</li><li>Provee una interfaz simple para instalar y personalizar</li><li>Previene el monitoreo de comunicación enmallada de Commotion</li><li>Previene ataques jamming/DoS contra el enmallado Commotion</li><li>Provee acceso sin electricidad</li><li>Provee encriptación fuerte</li><li>Provee protección de malware en dispositivos</li></ul>Con esta lista en mano redujimos los puntos que incrementan la habilidad de un usuario potencial para tomar una decisión informada sobre su seguridad.
Commotion no:
<ul><li>Provee anonimidad</li><li>Previene monitoreo del tráfico en Intenet</li><li>Provee seguridad fuerte sobre el enmallado</li><li>Resiste jamming o ataques DDoS</li><li>Protege tu dispositivo de Malware</li></ul>En <a href="https://commotionwireless.net/blog/warning-label-development-part-2">Parte 2</a>, vamos a repasar cómo utilizamos esta lista de características de seguridad no implementadas para desarrollar una etiqueta de advertencia.


