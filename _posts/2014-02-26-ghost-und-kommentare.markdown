---
layout: post
title: Ghost und Kommentare
date: '2014-02-26 20:45:50'
tags:
- disqus
- ghost-post
---

Bei [Ghost](http://www.ghost.org) sind keine Kommentare von Haus aus vorgesehen. Zumindest bislang nicht, eine einfache Möglichkeit dies nachzurüsten, wäre auf ein System wie [DisQus](http://www.disqus.com) zurückzugreifen. 

Der Einbau des 'Universalcodes' funktioniert gerade bei dem Standarttheme 'Casper' absolut einfach. Zu erst navigiert ihr zu folgender Datei:

> /ghost/content/themes/casper/post.hbs

Diese könnt ihr mit dem Editor eurer Wahl öffnen (z.B. auf dem *Terminal* mit *nano* oder eben auf euerm OS) und sucht nun folgende Stelle:

    <section class="post-content">
                {{content}}
            </section>
            
Hinter dem letzten Tag fügt ihr euern individuellen Code ein. Danach speichern (bei *nano* per ctrl+O und ctrl+X) und gegebenenfalls auf den Server schieben und den Ghost Service neustarten.

Auf einem Uberspace funktioniert das dann mit
> svc -h ~/service/ghost

Noch ein Wort zum Datenschutz:
Sämtliche Kommentare werden auf dem Server von DisQus gespeichert und unterliegen damit dem Gesetz der USA. Es empfiehlt sich also, zumindest im Adminmenü bei DisQus das anonyme kommentieren zu erlauben.

*UPDATE*
Falls ihr in der Titelzeile noch die Kommentaranzahl einpflegen wollt geht das wie folgt:

> index.hbs

öffnen und hier folgende Zeile suchen

    <span class="post-meta"><time datetime="{{date format='YYYY-MM-DD'}}">{{date format="DD MMM YYYY"}}</time> {{tags prefix="on "}}</span>

und ersetzen durch

    <span class="post-meta"><time datetime="{{date format='YYYY-MM-DD'}}">{{date format="DD MMM YYYY"}}</time> {{tags prefix="on "}} - <a href="{{url}}#disqus_thread">{{{title}}}</a></span>

danach öffnet ihr euch noch die

> default.hbs

und fügt vor das Ende des 

    </body>

hinzu

    <!-- DisQus --><br />
     <script type="text/javascript">
    /* * * CONFIGURATION VARIABLES: EDIT BEFORE PASTING INTO YOUR WEBPAGE * * */<br />
    var disqus_shortname = 'EUERBENUTZERNAME'; // required: replace example with your forum shortname

    /* * * DON'T EDIT BELOW THIS LINE * * */
    (function () {
        var s = document.createElement('script'); s.async = true;
        s.type = 'text/javascript';
        s.src = '//' + disqus_shortname + '.disqus.com/count.js';
        (document.getElementsByTagName('HEAD')[0] || document.getElementsByTagName('BODY')[0]).appendChild(s);
    }());
    </script>
    <!-- End DisQus --></code>

Wichtig ist, dass ihr **BENUTZERNAME** durch euern Adminnamen bei DisQus ersetzt.