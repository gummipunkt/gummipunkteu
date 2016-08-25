---
layout: post
title: Kindle Fire 7, Windows 10 und Google Play Store
date: '2015-12-26 11:34:46'
---

Es gibt ja einige Möglichkeiten den Google Play Store auf das Kindle Fire 7 zu bekommen, allerdings funktionieren diese nicht auf Anhieb mit Windows 10.

Um die ADB Treiber für Windows 10 zum laufen zu bekommen geht folgenden Weg:

1. Fire 7 an den Rechner anschließen, in den Fire Einstellungen auf Geräteoptionen und 7x auf die Seriennummer klicken, danach erscheinen die Entwickleroptionen darunter, hier bitte "ADB aktivieren" anklicken so das der nebenstehende Schalter "Orange" wird.

2. In die Suche "Geräte Manager" eingeben und dort das "Fire" finden, Doppelklick und Deinstallieren auswählen

3. ADB Setup herunterladen (V.1.4.3 funktioniert): http://forum.xda-developers.com/showthread.php?t=2588979

4. Die .exe installieren, danach wieder in den Gerätemanager, Doppelklick auf das Fire, danach auswählen Treiber vom Computer zu suchen und dann aus einer Liste installierter Treiber. Hier wählt Ihr Amazon Fire aus und darin den Google ADB Treiber.

4.1 Wieder in der Suche CMD eingeben und das Programm starten, hier gebt ihr: "adb devices" ein, dort sollte nun Eure Seriennummer erscheinen mit dem Wort device.

5. Weiter geht es mit dem "Amazon Fire 5th Gen Mod": http://forum.xda-developers.com/amazon-fire/general/installing-google-framework-playstore-t3216122

6. Entpacken und 1-Install-Play-Store auswählen und in dem neuen Fenster die Option auswählen den Play Store zu installieren.

Fertig.