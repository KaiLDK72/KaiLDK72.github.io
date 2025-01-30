---
title: Alle Zugriffe ohne WWW auf Seiten mit WWW voran umleiten
---

Das geht relativ einfach über die .htaccess Datei.
In dieser einfach das einfügen:
```bash
RewriteEngine On
RewriteCond %{HTTP_HOST} !^www\. [NC]
RewriteRule ^(.*)$ http://www.%{HTTP_HOST}/$1 [R=301,L]
```
Das geht dann auch mit HTTPS wenn man, wie man eigentlich immer sollte, ohnehin bei HTTP Zugriffen
auf HTTPS umleitet.

