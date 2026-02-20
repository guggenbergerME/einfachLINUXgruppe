# Linux Gruppe

## Inhaltsverzeichnis

- [Programme installieren](#programme-installieren)
- [Videokonferenzen](#videokonferenzen)
- [Fernwartung / Remote](#fernwartung--remote)
- [Terminal-Befehle](#terminal-befehle)
- [USB-Bootstick erstellen](#usb-bootstick-erstellen)
- [Alternative zur FritzBox mit OPNsense](#alternative-zur-fritzbox-mit-opnsense)
- [Systemsicherung mit Timeshift](#systemsicherung-mit-timeshift)
- [Schreibtisch anpassen](#schreibtisch-anpassen)
- [BIOS / Boot-Menü – Tastenkombinationen und Einstellungen](#bios--boot-menü--tastenkombinationen-und-einstellungen)
- [Nostr – Dezentrales Kommunikationsprotokoll](#nostr--dezentrales-kommunikationsprotokoll)

---

## Programme installieren

Anleitungen zur Installation von Programmen unter Linux.

+ [Zur Übersicht](Prog_installieren/Readme.md)

---

## Videokonferenzen

+ [Zur Übersicht](Videokonferenz-Plattform/Readme.md)

---

## Fernwartung / Remote

Anleitungen zur Fernwartung und Remote-Unterstützung.

+ [Zur Übersicht](Fernwartung_Remote/Readme.md)

---

## Terminal-Befehle

Die wichtigsten Befehle für das Terminal unter Linux Mint.

+ [Zur Übersicht](Terminal-Befehle/Readme.md)

---

## USB-Bootstick erstellen

Anleitung zum Erstellen eines bootfähigen Linux-USB-Sticks unter Windows.

+ [Zur Anleitung](USB-Bootstick/Readme.md)

---

## Alternative zur FritzBox mit OPNsense

Router und Firewall für zuhause – als Open-Source-Alternative zur FritzBox.

+ [Zur Übersicht](OPNsense/Readme.md)

---

## Systemsicherung mit Timeshift

Snapshots erstellen und das System bei Problemen schnell wiederherstellen.

+ [Zur Anleitung](Timeshift/Readme.md)

---

## Schreibtisch anpassen

Hintergrundbild, Design, Schriftgröße, Taskleiste und mehr – für Einsteiger erklärt.

+ [Zur Anleitung](Schreibtisch-anpassen/Readme.md)

---

## BIOS / Boot-Menü – Tastenkombinationen und Einstellungen

Beim Starten des Computers kann man über bestimmte Tasten ins **BIOS/UEFI** oder direkt ins **Boot-Menü** gelangen. Das ist nötig, um z. B. von einem USB-Stick zu booten.

### Tastenkombinationen nach Hersteller

#### Notebooks / Laptops

| Hersteller | BIOS/UEFI aufrufen | Boot-Menü |
|---|---|---|
| **Lenovo** | F2 oder Fn+F2 | F12 |
| **HP** | F10 oder Esc | F9 oder Esc |
| **Dell** | F2 | F12 |
| **ASUS** | F2 oder Entf | F8 oder Esc |
| **Acer** | F2 oder Entf | F12 |
| **MSI** | Entf | F11 |
| **Toshiba / Dynabook** | F2 | F12 |
| **Samsung** | F2 | F10 |
| **Fujitsu** | F2 | F12 |
| **Medion** | F2 oder Entf | F12 oder Esc |

#### Desktop-PCs / Mainboards

| Hersteller | BIOS/UEFI aufrufen | Boot-Menü |
|---|---|---|
| **ASUS** | Entf oder F2 | F8 |
| **MSI** | Entf | F11 |
| **Gigabyte** | Entf | F12 |
| **ASRock** | F2 oder Entf | F11 |
| **Biostar** | Entf | F9 |
| **Intel** | F2 | F10 |

#### Sonstige

| Gerät / System | BIOS/UEFI aufrufen | Boot-Menü |
|---|---|---|
| **Apple Mac (Intel)** | – | Alt/Option (⌥) gedrückt halten |
| **Microsoft Surface** | Lautstärke+ beim Einschalten halten | – |

> **Tipp:** Die Taste muss **sofort nach dem Einschalten** wiederholt gedrückt werden – noch bevor das Betriebssystem startet.

### BIOS-Einstellungen zum Booten vom USB-Stick

Wenn der Computer den USB-Stick nicht automatisch erkennt oder nicht davon bootet, müssen im BIOS/UEFI folgende Einstellungen geprüft und ggf. angepasst werden:

#### 1. Boot-Reihenfolge ändern

Im BIOS unter dem Menüpunkt **Boot** (oder **Boot Order** / **Boot Priority**) die Reihenfolge so ändern, dass der **USB-Stick vor der Festplatte** steht. Damit versucht der Computer zuerst vom USB-Stick zu starten.

#### 2. Secure Boot deaktivieren

**Secure Boot** verhindert das Starten von nicht signierten Betriebssystemen. Für die meisten Linux-Installationen sollte Secure Boot **deaktiviert** werden:

- Im BIOS unter **Security** oder **Boot** den Eintrag **Secure Boot** suchen
- Auf **Disabled** setzen

> **Hinweis:** Linux Mint und Ubuntu unterstützen Secure Boot grundsätzlich. Falls es trotzdem Probleme beim Booten gibt, Secure Boot testweise deaktivieren.

#### 3. Boot-Modus: UEFI vs. Legacy (CSM)

Moderne Computer verwenden **UEFI**. Ältere Systeme nutzen das klassische **BIOS (Legacy)**. Der USB-Stick muss zum Boot-Modus passen:

- **UEFI-Modus** (empfohlen für neuere PCs): USB-Stick mit **GPT** erstellt (z. B. in Rufus)
- **Legacy/CSM-Modus** (für ältere PCs): USB-Stick mit **MBR** erstellt

Falls der USB-Stick nicht im Boot-Menü auftaucht, kann es helfen, den jeweils anderen Modus zu aktivieren oder **CSM (Compatibility Support Module)** einzuschalten.

#### 4. Fast Boot deaktivieren

Manche BIOS-Versionen haben eine **Fast Boot**-Option, die den Startvorgang beschleunigt, dabei aber USB-Geräte beim Booten überspringt. Falls der USB-Stick nicht erkannt wird:

- Im BIOS unter **Boot** den Eintrag **Fast Boot** suchen
- Auf **Disabled** setzen

---

## Nostr – Dezentrales Kommunikationsprotokoll

**Nostr** steht für **„Notes and Other Stuff Transmitted by Relays"** und ist ein offenes, dezentrales Protokoll für soziale Kommunikation im Internet.

### Was ist Nostr?

Nostr ist kein einzelnes Programm oder eine Plattform, sondern ein **Protokoll** – also ein Regelwerk, nach dem verschiedene Apps und Server (sogenannte **Relays**) miteinander kommunizieren. Jeder kann einen eigenen Relay betreiben, und Nutzer können frei wählen, über welche Relays sie kommunizieren. Es gibt keine zentrale Firma und keinen einzelnen Server, der alles kontrolliert.

Die eigene Identität basiert auf einem **kryptografischen Schlüsselpaar** (öffentlicher und privater Schlüssel). Damit behält man die volle Kontrolle über sein Konto – ohne E-Mail-Adresse, Telefonnummer oder Passwort bei einem Anbieter.

### Vorteile von Nostr

- **Dezentral:** Es gibt keinen zentralen Server. Fällt ein Relay aus, funktioniert das Netzwerk über andere Relays weiter.
- **Zensurresistent:** Kein einzelner Betreiber kann Inhalte für alle löschen oder Nutzer dauerhaft sperren.
- **Keine Registrierung nötig:** Ein Schlüsselpaar genügt – kein Benutzername, keine E-Mail, kein Passwort bei einem Drittanbieter.
- **Eigentum an der eigenen Identität:** Der private Schlüssel gehört nur dem Nutzer. Man ist nicht von einer Plattform abhängig.
- **Offenes Protokoll:** Jeder kann eigene Apps (Clients) oder Relays entwickeln. Es gibt bereits Clients für Kurznachrichten, Chats, Blogs und mehr.
- **Keine Werbung und kein Tracking:** Das Protokoll selbst sammelt keine Daten und zeigt keine Werbung.
- **Plattformübergreifend:** Nostr-Clients gibt es für Linux, Windows, macOS, Android und iOS.
- **Interoperabel:** Egal welchen Client man nutzt – alle greifen auf dasselbe Netzwerk zu. Man ist nicht an eine einzelne App gebunden.
