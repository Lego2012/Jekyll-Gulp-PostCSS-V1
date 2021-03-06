# Dieses Respository wird nicht weiter gepflegt, kann aber natürlich weiter genutzt werden
# Leo's Jekyll Template powered by Gulp und PostCSS
#### Inspiriert von [stefanimhoff.de](http://stefanimhoff.de/)

## Aktuell ist der Branch `develop`!

## Installation
Klone das Repository auf Deinen Computer und wechsle in den Projektordner. Starte:

```sh
$ ./install-dev.sh
```

Damit werden automatisch `bundle`, `bower install` und `npm install` gestartet. Außerdem wird die `normalize.css` in das CSS-Verzeichnis kopiert. Die `main.css` importiert diese Datei dann automatisch.

Um [Fontcustom](http://fontcustom.com/) zu installieren, solltest Du [Homebrew](http://brew.sh/) installiert haben oder ein anderes Paketmanagementwerkzeug nutzen um die Abhängigkeiten zu installieren:

```sh
$ brew install fontforge --with-python
$ brew install eot-utils
```

## Setup

Öffne `gulpFiles/config.js` und ändere die Einstellungen falls nötig. Nur die `rsync` Einstellungen müssen tatsächlich angepasst werden. Ändere `destination` zum Pfad Deines Webservers und ändere `hostname` und `username`.

## Gulp.js starten

Drei Tasks sind verfügbar:

```sh
$ gulp
$ gulp publish
$ gulp deploy
```

- `gulp` startet den Entwicklungsserver, baut die Assets zusammen, erstellt die Jekyll Site und startet einen `watch` task.
- `gulp publish` kopiert und optimiert die Assets und startet ein Production-Build von Jekyll.
- `gulp deploy` transferiert die generierten Dateien mit Rsync auf den Server.
