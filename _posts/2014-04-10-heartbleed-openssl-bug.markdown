---
layout: post
title: Heartbleed - OpenSSL Bug
date: '2014-04-10 08:02:20'
tags:
- netzgefluster
---

Nur um es kurz einmal festzuhalten und auch direkt am Anfang:
Der OpenSSL-Bug "Heartbleed" ist weder ein Beweis für noch gegen OpenSource-Software gegenüber ClosedSource.
Das ist vollkommener Schwachsinn anhand dessen irgendein "Format" positiver oder negativer darzustellen.

Aber wer ist denn eigentlich Schuld daran? Gibt es einen Schuldigen? Den Programmierer? Derjenige der das entsprechende Stück Code in OpenSSL aufgenommen hat?
Braucht es überhaupt einen Schuldigen? Kann das nicht einfach ein doofer Fehler sein?

Wir reden bei OpenSSL über Software, denen Menschen vertraut haben, damit verschlüsselt Daten übertragen zu können. Für diesen Grund, wurde OpenSSL entwickelt, herausgebracht und genutzt. Wenn ich Software schreibe die Sicherheit garantieren soll, dann muss ich dafür Sorgen, dass dieser Zweck erfüllt wird. Zumindest in einem Maße, der vertretbar ist und gerade im Falle von Heartbleed war das ja - jetzt im Nachhinein - durchaus vermeidbar.

Hier hat nicht nur der Programmierer versagt, sondern auch der Maintainer der es eingepflegt hat. Aber nicht nur diese zwei haben versagt, sondern auch die großen IT Firmen. Nehmen wir nur mal zwei: Google und Yahoo. Beide haben OpenSSL in Version 1.01 eingesetzt und den Code nicht oder nicht ordentlich auditieren lassen bzw selbst geprüft.

Ich erwarte verdammt nochmal, dass Firmen mit fast unbegrenzten Geldmengen nicht nur die eigene Software ordentlich überprüfen lassen, sondern auch das was von außerhalb kommt. Sei es Closed- oder OpenSource. Gerade bei letzterem ist zwar irgendwann "Big G" darauf gestoßen, aber deutlich zu spät. 

Ich sehe also einen Haufen Menschen, die in diesem Fall versagt haben.	