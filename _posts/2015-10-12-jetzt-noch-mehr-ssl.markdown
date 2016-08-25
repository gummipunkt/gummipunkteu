---
layout: post
title: Jetzt noch mehr SSL
date: '2015-10-12 08:26:58'
---

Ich habe es nun ewig vor mir hergeschoben dem Blog ein SSL Zertifikat zu spendieren. Klar, hier gibt es nichts was verschlüsselt übertragen werden müsste, aber es erhöht zumindest das Grundrauschen bei den Geheimdiensten.

Mit *WoSign* gibt es im Huckepack ein kostenloses und dreijähriges SSL Zertifikat für Domain.tld als auch www.Domain.tld.

*Ghost* kann automatisch auf einem *uberspace* in https deployen (einfach in der config.js alle http auf https ändern), sodass jeder automatisch nun von http auf https umgeleitet wird. Eine Anleitung gibt es bei [yaut.de](https://blog.yaut.de/2015/06/ssl-uberspace-und-wosign/)!

Im übrigen haben die [uberspaceler](https://www.uberspace.de) das Zertifikat innerhalb von fünf Minuten in den Apache eingebaut. Danke <3