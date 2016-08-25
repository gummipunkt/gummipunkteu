---
layout: post
title: Google weiß es - Zeit was zu ändern
date: '2014-03-07 09:52:28'
tags:
- datenschutz
- google
- android
---

Ich nutze nun schon über zehn Jahre viele Dienste von Google.

* Google Suche
* Google Mail
* Google Maps
* Google Chrome
* Android
	* PlayStore
    * Google Music
* Google Kalender (CalDav Support!)
* Google Picasa
* Google Plus
* Google Drive

Natürlich ist es mir durchaus - und auch mit etwas Bauchweh - bewusst, wie kritisch es ist seine eigenen Daten nur bei einem Konzern abzulegen. Gerade das nutzen von Android macht die Sache unfassbar einfach im Zusammenspiel mit einem Desktop-PC Dinge synchron zu halten und ja, es ist nett wenn ich den Verlauf vom Desktop auf das Smartphone bekomme.

Nun hat Google allerdings mal wieder sein [Dashboard](https://www.google.com/settings/dashboard) aktualisiert und führt dort alle Daten zusammen. Was Vorbildlich ist, hat mir gleichzeitig auch die Augen geöffnet.

Exemplarisch GMail:
![Dashboard Analyse GMail](/content/images/2014/Mar/gmail.png)

und Picasa:
![Dashboard Picasa](/content/images/2014/Mar/gpicasa.png)

Man stelle sich nun mal nicht vor, dass ein Google Mitarbeiter mich stalken möchte oder Hacker an mein Google Passwort kommen, sondern das Sicherheitsbehörden oder die Polizei auf offiziellem Wege Zugriff erlangen:

Meine sämtlichen Suchaktivitäten sind gespeichert, jede Mail, jedes Foto und jede Mapsaktivität ist zugänglich.

Damit muss und wird Schluss sein. Heute beginnt der digitale Umzug aus dem Schoße Googles ab in die eigene Infrastruktur mit getrennten Zugangspasswörtern, getrennte Hoster und verschiedener Software.

#### Browser

Der kleinste Schritt ist erst einmal Weg von Chrome. Alternativen gibt es glücklicherweise:

* Firefox
* Opera

Während Firefox unter der Mozilla Stiftung Open Source ist, kommt Opera aus einer properitären Ecke. 

#### Suchmaschine

Die richtige Wahl der Suchmaschine ist so eine Sache, denn immerhin sind für mich die Ergebnisse von Google deutlich besser, als das was Bing, Ask, Yahoo oder andere ausspucken. Eine META-Suchmaschine wäre daher die richtige Wahl. Diese greift mehrere Suchmaschinen ab und füttert so die eigene Ausgabe, teilweise ist es möglich die Suchmaschinen zu beschränken. Die Wahl fällt eindeutig auf [DuckDuckGo](https://duckduckgo.com/). 
Anonymes Suchen mit den Ergebnissen von Google: Zwei Fliegen mit einer Klappe schlagen. Wichtig dabei: Natürlich kann der Traffic weiter mitgeschnitten werden und theoretisch könnte DDG trotz anderer Versprechen trotzdem Logs führen. 

#### Mail
Jetzt wird es aufwendiger: Wir brauchen einen neuen Mailanbieter. Neben den klassischen Betreibern wie UnitedInternet (GMX, Web.de) oder Yahoo bietet sich vor allem die Möglichkeit an, auf eine eigene Domain mit Mailserver zu setzen.

Viele Hostinganbieter bieten die Möglichkeit, mehrere GB an Mailspeicher plus eigener Domain für einen monatlichen Paketpreis zu mieten.

Alternativ gibt es auch Anbieter wie [Uberspace](https://www.uberspace.de) die einen vorinstallierten Mailserver anbieten, dazu gibt es [Scripts](http://www.fidepus.de/2013/04/05/e-mails-von-gmail-zu-uberspace-umziehen/) die den kompletten GMail Account auslesen und dorthin verschieben.

Bis alle Kontakte die neue Mailadresse nutzen, kann man eine Weiterleitung von seiner GMail- auf die neue Mailadresse weiterlaufen lassen.

#### Maps

Hier sei einem jedem die gute Alternative [OpenStreetMap](https://www.openstreetmap.org) an das Herz gelegt. Meist sehr gute Kartenqualität und viele Programme, Scripts und Apps die auf diese Kartenbasis zugreifen.

#### Kalender, Picasa & Drive

Hier kommt die All-in-One Lösung [OwnCloud](http://owncloud.org/) zum tragen. Kalender mit CalDav Support, Foto- und Dateimanager mit ausgeklügelter Sharing Lösung.
Auch hier kann man aus mehreren Anbietern wählen und ruck zuck sind die eigenen Daten wieder in unserem Besitz.

Gerade macht sich auch BTSync auf den Weg, ein eigenes Cloud Konzept zu entwickeln. Hier befindet sich das ganze noch in einer Beta Phase, sollte man aber gleichzeitig mal ausprobieren. Allerdings würde das "nur" Google Drive ersetzen, für Kalender und Fotos müsste man einen anderen Weg suchen.

#### Google Plus (und Facebook)

Zu Google+ und Facebook gibt es natürlich eine Alternative: [Diaspora](https://joindiaspora.com/), aber wie das so ist mit den sozialen Netzwerken, steht und fällt so ein Projekt mit der Nutzerzahl im eigenen Freundes- und Bekanntenkreis. Ich kann also nur empfehlen: Meldet euch dort an, bespaßt euer Profil und versucht immer wieder Leute dahinzuziehen (auch über G+ und FB Posts) und teilt auf den bekannten Netzwerken nur das, was die ganze Welt auch wirklich von euch wissen dürfte. Den Rest solltet ihr euch sparen.


#### Android

Das Smartphone Betriebssystem Android ist natürlich so eine eigene Sache, weil kaum verzichtbar. Freie Alternativen wie Firefox OS oder UbuntuOS laufen momentan noch auf sehr wenigen Smartphones und die Auswahl im AppStore ist relativ bescheiden. 

Punkten dagegen können modifizierte AOSP Android Systeme wie [Paranoid Android](http://paranoidandroid.co/) die einen starken Wert auf einen guten Datenschutz legen.