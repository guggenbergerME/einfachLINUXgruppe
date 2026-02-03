# TOR Browser installieren

## ✅ Empfohlene Methode: Über die offizielle Tor-Website

Das ist der sicherste und aktuellste Weg.

### 1. Tor Browser herunterladen

Öffne deinen normalen Browser

Geh auf: https://www.torproject.org

Klick auf Download Tor Browser

Wähle Linux (64-bit)

Du bekommst eine Datei wie:

```
tor-browser-linux-x86_64-<version>.tar.xz
```

### 2. Archiv entpacken

Öffne ein Terminal im Download-Ordner und gib ein:

```
tar -xvf tor-browser-linux-x86_64-*.tar.xz
```

Danach gibt es einen neuen Ordner:

```
tor-browser/
```

### 3. Tor Browser starten

Wechsle in den Ordner und starte das Installationsskript:

```
cd tor-browser
./start-tor-browser.desktop
```

Beim ersten Start:

Installation bestätigen

### Daten lassem sich nicht installieren
Wenn der Launcher keinen Download ziehen kann wir die Anfrage von TOR von dem aktuellen Internetprovider gesperrt. Einfach einen andern Hotspot oder Internetprvider probiern.


Sprache wählen

Optional: Desktop-Verknüpfung anlegen

👉 Danach kannst du Tor ganz normal über das Startmenü öffnen.

Tor Browser einfach per flathub oder Repo installieren.

Sollte kein Download des Launchers erfolgen, liegt einen Netzwerksperre des Internetanbieter vor.