# Fernwartung für Gruppenmitglieder

## Rustdesk

### RustDesk herunterladen

Geh auf die offizielle Seite:
👉 https://rustdesk.com

Klick auf Download

Wähle Linux → Debian/Ubuntu (.deb)
(Linux Mint ist Ubuntu-basiert, passt also perfekt)

### Paket installieren

Öffne ein Terminal im Download-Ordner und tippe:

```
sudo apt install ./rustdesk-*.deb
```

Oder ganz bequem:

Doppelklick auf die .deb-Datei

Softwareverwaltung → Installieren

### Starten

Menü → RustDesk

Fertig 🎉

### Konfigurieren
Um Rustdesk zu nutzen ist eine Konfiguration notwendig. Die kann per Anleitung oder per Datei erfolgen.

📍 Wo liegt die RustDesk1.toml unter Linux Mint?
👉 Für deinen Benutzer
~/.config/rustdesk/RustDesk1.toml

Ausgeschrieben:

/home/DEIN_BENUTZERNAME/.config/rustdesk/RustDesk1.toml

👉 Prüfen im Terminal:

ls ~/.config/rustdesk/