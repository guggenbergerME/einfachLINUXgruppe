# Wichtige Terminal-Befehle für Linux Mint

## Inhaltsverzeichnis

- [Terminal öffnen](#terminal-öffnen)
- [Navigation & Dateiverwaltung](#navigation--dateiverwaltung)
- [Dateien anzeigen & bearbeiten](#dateien-anzeigen--bearbeiten)
- [Suchen & Filtern](#suchen--filtern)
- [System & Updates](#system--updates)
- [Systeminformationen](#systeminformationen)
- [Prozesse verwalten](#prozesse-verwalten)
- [Netzwerk](#netzwerk)
- [Benutzer & Berechtigungen](#benutzer--berechtigungen)
- [Archive & Komprimierung](#archive--komprimierung)

---

## Terminal öffnen

```
Strg + Alt + T
```

---

## Navigation & Dateiverwaltung

| Befehl | Beschreibung |
|--------|-------------|
| `pwd` | Aktuelles Verzeichnis anzeigen |
| `ls` | Dateien und Ordner auflisten |
| `ls -la` | Ausführliche Liste inkl. versteckter Dateien |
| `cd Ordnername` | In einen Ordner wechseln |
| `cd ..` | Einen Ordner zurück |
| `cd ~` | Ins Home-Verzeichnis wechseln |
| `mkdir Ordnername` | Neuen Ordner erstellen |
| `rm Datei` | Datei löschen |
| `rm -r Ordner` | Ordner mit Inhalt löschen |
| `cp Quelle Ziel` | Datei oder Ordner kopieren |
| `mv Quelle Ziel` | Datei oder Ordner verschieben / umbenennen |

---

## Dateien anzeigen & bearbeiten

| Befehl | Beschreibung |
|--------|-------------|
| `cat Datei` | Dateiinhalt anzeigen |
| `less Datei` | Datei seitenweise anzeigen (q zum Beenden) |
| `nano Datei` | Datei im Terminal-Editor öffnen |
| `touch Datei` | Leere Datei erstellen |

---

## Suchen & Filtern

| Befehl | Beschreibung |
|--------|-------------|
| `find . -name "*.txt"` | Dateien nach Name suchen |
| `grep "Begriff" Datei` | Text in Datei suchen |
| `grep -r "Begriff" .` | Text in allen Dateien im Ordner suchen |
| `history` | Letzte Befehle anzeigen |
| `history \| grep apt` | In der Befehlshistorie suchen |

---

## System & Updates

```bash
sudo apt update
```
Paketlisten aktualisieren (immer zuerst ausführen)

```bash
sudo apt upgrade
```
Alle installierten Pakete aktualisieren

```bash
sudo apt install Paketname
```
Programm installieren

```bash
sudo apt remove Paketname
```
Programm deinstallieren

```bash
sudo apt autoremove
```
Nicht mehr benötigte Pakete aufräumen

---

## Systeminformationen

| Befehl | Beschreibung |
|--------|-------------|
| `uname -a` | Kernel-Version und Systeminfos |
| `lsb_release -a` | Linux-Distribution und Version |
| `df -h` | Festplattenspeicher anzeigen |
| `free -h` | Arbeitsspeicher anzeigen |
| `top` | Laufende Prozesse und Auslastung (q zum Beenden) |
| `htop` | Erweiterte Prozessansicht (muss ggf. installiert werden) |
| `uptime` | Wie lange läuft das System schon |

---

## Prozesse verwalten

| Befehl | Beschreibung |
|--------|-------------|
| `ps aux` | Alle laufenden Prozesse anzeigen |
| `kill PID` | Prozess mit bestimmter ID beenden |
| `killall Programmname` | Alle Prozesse eines Programms beenden |
| `systemctl status Dienst` | Status eines Systemdienstes prüfen |
| `sudo systemctl start Dienst` | Dienst starten |
| `sudo systemctl stop Dienst` | Dienst stoppen |
| `sudo systemctl restart Dienst` | Dienst neu starten |

---

## Netzwerk

| Befehl | Beschreibung |
|--------|-------------|
| `ping google.com` | Verbindung testen (Strg+C zum Stoppen) |
| `ip a` | Netzwerkschnittstellen und IP-Adressen anzeigen |
| `wget URL` | Datei aus dem Internet herunterladen |
| `curl URL` | URL abrufen oder Datei herunterladen |
| `ss -tuln` | Offene Ports anzeigen |

---

## Benutzer & Berechtigungen

| Befehl | Beschreibung |
|--------|-------------|
| `whoami` | Aktuellen Benutzernamen anzeigen |
| `sudo Befehl` | Befehl als Administrator ausführen |
| `chmod +x Datei` | Datei ausführbar machen |
| `chmod 644 Datei` | Berechtigungen setzen (Besitzer lesen/schreiben, andere lesen) |
| `chown Benutzer Datei` | Dateibesitzer ändern |

---

## Archive & Komprimierung

| Befehl | Beschreibung |
|--------|-------------|
| `tar -xvf archiv.tar.xz` | tar.xz-Archiv entpacken |
| `tar -cvf archiv.tar Ordner` | Ordner als tar-Archiv packen |
| `unzip archiv.zip` | ZIP-Datei entpacken |
| `zip -r archiv.zip Ordner` | Ordner als ZIP packen |

---

> **Tipp:** Mit der Pfeiltaste nach oben kannst du zuletzt eingegebene Befehle wiederholen. Mit `Tab` wird ein Befehl oder Dateiname automatisch ergänzt.
