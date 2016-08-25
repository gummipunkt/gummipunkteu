---
layout: post
title: "#Minecraft Server auf #Uberspace betreiben"
date: '2015-11-19 10:00:19'
---

Einen Minecraft Server auf einem Uberspace Account betreiben? Dank Cuberite geht das ziemlich einfach und schnell. 

Kleine Einschränkung: Maximal neun Spieler und zwei Welten. Allerdings gibt es dafür Support von den Minecraft-Versionen 1.7, 1.8 und 1.9.

Also, per SSH auf deinem Uberspace einloggen und los geht es:

1) Falls noch nicht passiert "gcc5" als Standard aktivieren:
> echo "export PATH=/package/host/localhost/gcc-5/bin:$PATH" >> ~/.bashrc

> source ~/.bashrc

2) per Toast "cmake" installieren
> toast arm cmake 

3) Weiter zu cuberite
> cd ~/
 
>bash -c "$(curl https://raw.githubusercontent.com/cuberite/cuberite/master/compile.sh)"

3.1) Nun könnt Ihr aussuchen welche Branch Ihr möchtet: Stable, Beta oder Dev. Als Build Typ wählt ihr "Normal"

4) Ab ins richtige Verzeichnis wechseln
> cd ~/cuberite/Server

5) Starten von Cuberite damit die letzten Daten angelegt werden
> ./Cuberite

6) Nachdem Cuberite gestartet ist, beendet Ihr den Server per "STRG + C"

7) Nun braucht Ihr zwei freie Ports auf Euerm Uberspace. Der muss > 61000 und < 65535 sein. Ob ein Port noch frei ist, könnt Ihr mit dem Befehl
> netstat -tulpen | grep PORTNUMMER

prüfen. Kommt keine Ausgabe, ist der Port frei. Dann sendet eine Mail an "hallo@uberspace.de" mit eurem Benutzernamen, eurem Server, den beiden Ports mit der bitte die freizuschalten als TCP.

8) Editieren der settings.ini
> vim ~/Cuberite/Server/settings.ini

8.1) mit "i" wechselt Ihr in den "edit"-Mode und ändert es wie folgt ab:
> [Authentication]
Authenticate=0 # hier 1 falls man sich Authentifizieren soll
AllowBungeeCord=0
Server=EURE_DOMAIN_ODER_UBERSPACE_LINK
Address=/session/minecraft/hasJoined?username=%USERNAME%&serverId=%SERVERID%
>
[MojangAPI]
NameToUUIDServer=api.mojang.com
NameToUUIDAddress=/profiles/minecraft
UUIDToProfileServer=sessionserver.mojang.com
UUIDToProfileAddress=/session/minecraft/profile/%UUID%?unsigned=false
>
[Server]
Description=EUER_MINECRAFT_SERVER_NAME
MaxPlayers=8 # Maximale Playeranzahl
HardcoreEnabled=0
AllowMultiLogin=0
Ports=ERSTER_FREIER_PORT_DEN_IHR_AN_UBERSPACE_GESENDET_HABT

auf eure Daten ab. Mit "ESC" und ":wq!" speichert und schließt Ihr das Dokument unter vim.

9) Weiter geht es mit dem Webadmin
> vim ~/Cuberite/Server/webadmin.ini

9.1) Wieder mit "i" in den edit-Modus wechseln und Daten eingeben

> [WebAdmin]
Ports=ZWEITER_FREIER_PORT
Enabled=1 # Bei 0 wäre Webadmin aus
>
[User:EUER_USERNAME]
Password=EUER_PASSWORT

10) Leider kann man für Cuberite (noch) keinen uberspace Service aufsetzen, so muss uns "screen" helfen. Den Server startet man im Server Verzeichnis und dem Befehl "./Cuberite".

10.1) Screen anlegen und Cuberite starten
> screen -S cuberite

> cd ~/cuberite/Server

> source ~/.bashrc

> ulimit -c unlimited

>./Cuberite

Nachdem der Server gestartet hat per

> STRG + A und "D"

screen wieder in den Hintergrund schieben.

Mit dem Befehl 
> screen -R cuberite

kommt Ihr wieder auf die Kommandozeile von Cuberite. Diesen könnt Ihr mit STRG + C beenden.

11) Auf die Adminoberfläche kommt Ihr mit Eurer Domain.xx:ZWEITER_PORT



