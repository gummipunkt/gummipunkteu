---
layout: post
title: Jabber Server und Webclient
date: '2014-02-09 07:55:34'
tags:
- jabber
- jabber-server
- jabber-client
- jabber-web-client
- xmpp
---

Ich habe mich gestern Abend mal wieder um einen Jabberserver bemüht und endlich mit **Openfire** das auch mal umgesetzt, gleichzeitig habe ich als Webclient **Sparkweb** aufgesetzt.

Openfire läuft auf einem eigenen Server ohne Apache Modul und mit einer strikten iptable die rein auf die Openfire benötigten Ports eingestellt ist. Denkt aber bitte daran, Jabber mit SSL ist kein Ersatz für eine ordentliche Verschlüsselung a la PGP. 

Ihr findet alle wichtigen Informationen hier:
[Jabber Server](/jabber-server/)

Eine Registrierung erfolgt im übrigen nicht über ein Webinterface, sondern direkt aus dem Jabber Client heraus, sollte dieses von eurem nicht unterstützt werden, nutzt für die Registrierung den Webclient.