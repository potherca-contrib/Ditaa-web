What is Ditaa
=============

[Ditaa](http://ditaa.sourceforge.net/) is a magical wand wich convert ascii-art scheme into nice picture.
The original tool only work as a command line tool.
This variants bring ditaa to webservice hype.

Now, ditaa  can be efficiently used from a webserver (as a wiki filter), even in a mutualised server.

Use DAS, Ditaa As a Service
===========================

Put ditaa\_web.war in your favorite servlet container (glassfish, jetty, tomcat ...).
From the client side, Ditaa is accessed with a simple POST request with this arguments :

 * _ditaa_ the scheme.
 * _no-antialias_
 * _no-shadows_
 * _scale_
 * _round-corners_
 * _no-separations_

Don't forget to add caching.

A PHP and Python example are provided.

Build it
========

Java
----

This project use Maven2 for its build. Maven will download a lot of craps, but after that, you wille be able to test it without pain.

	$ cd java
	$ mvn jetty:run
	
You can test it at [http://localhost:8080/DitaaWeb/ditaa](http://localhost:8080/DitaaWeb/ditaa)

	$ mvn package

Build the war packet for your servlet container

Snow leopard provides a decent maven2, and any linux must have a package with maven2

Php
---

Php doesn't need build. Just copy the class and reads the example.

Python
------

Read the source, and try it. You can hack the webservice url with your own servlet :

	$ cd python
	$ ./ditaa.py

Trac
----

[Trac](http://trac.edgewall.org/) is a nice bug tracker with a wiki tool. The work is stolen from the graphviz module

	$ cd trac
	$ python setup.py install

Drupal
------

[Drupal](http://drupal.org) is a CMS. [Drupal-Ditaa](http://github.com/athoune/Drupal-Ditaa) got its own github.
