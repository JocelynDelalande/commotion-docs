---
layout: blog
title: An audit of current Commotion user interfaces
categories: UI,UX,Research
created: 2012-05-09
changed: 2013-07-26
post_author: The Work Department
lang: en
---
  <div class="field-content"><p>With the goal of creating both an intuitive and accessible user experience (UX) across a sampling of devices that will run Commotion, we surveyed and analyzed the current state of the existing interfaces. We deployed a test network using the three software components currently in development phases: Commotion on an Ubiquiti Picostation (router), The Guardian Project&rsquo;s OLSR Mesh Tether on an Android handset (phone) and Commotion on Linux (laptop). In anticipation of The Serval Project&rsquo;s forthcoming work around meshing mobile devices with Commotion, we also researched the current release of Serval Mesh. We documented each step with screenshots, <a href="http://www.flickr.com/photos/24639042@N07/collections/72157629382917618/" target="blank">which are compiled here</a>.</p>
<p>After the initial audit, we compared and contrasted each workflow, documenting any issues that arose during the process and were then able to make recommendations on how to improve each of the interfaces and workflows and make them consistent across platforms.</p>
<pre class="text geshifilter-text" style="font-family:monospace;">
# add guardian&#39;s ppa
apt-get update
apt-get install olsrd
# edit /etc/olsrd/olsrd.conf: set DebugLevel to 1, change Interface to your wifi card
sudo service stop network-manager
sudo ifconfig wlan0 up
sudo ifconfig wlan0 5.70.60.60 netmask 255.0.0.0
olsrd -f /etc/olsrd/olsrd.conf</pre>
</div><p><strong>Shared actions: Commotion router, OLSR Mesh Tether phone and Serval Mesh phone</strong></p>
<p>The Commotion Router and Serval Mesh processes start with a splash page that includes a welcome/warning, more information, and the choice to either continue or cancel. The OLSR Mesh Tether and Commotion Linux processes don&rsquo;t have any initial instruction or more information about the software. From this point in the workflow, all of the processes become equally unclear as to what is necessary to configure the network. The Commotion Linux and OLSR Mesh Tether interfaces are the least informative. The OLSR Mesh Tether user interface (UI) offers only a few hints as to what is optional and rarely defines terminology. The Linux application, as it is run from the terminal, offers no hints or help at all. The Commotion Router UI has the most information - because it is accessed from a laptop and not a handheld device, there is plenty of &ldquo;space&rdquo; to feature this much detail. But while there is more detail and are more options, there is no guidance and the process far from intuitive. As auditors, we conclude that without programming or mesh-networking experience, the chances for users to successfully configure a network are slim.</p>