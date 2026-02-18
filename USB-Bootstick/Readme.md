# USB-Bootstick für Linux unter Windows erstellen

Mit einem USB-Bootstick kannst du Linux Mint auf deinem Computer installieren oder ausprobieren, ohne es sofort zu installieren.

## Inhaltsverzeichnis

- [Was du brauchst](#was-du-brauchst)
- [Schritt 1: Linux Mint ISO herunterladen](#schritt-1-linux-mint-iso-herunterladen)
- [Schritt 2: Rufus herunterladen](#schritt-2-rufus-herunterladen)
- [Schritt 3: Bootstick erstellen](#schritt-3-bootstick-erstellen)
- [Schritt 4: Vom USB-Stick booten](#schritt-4-vom-usb-stick-booten)

---

## Was du brauchst

- Einen USB-Stick mit **mindestens 8 GB** Speicher
- Das Programm **Rufus** (kostenlos, kein Install nötig)
- Die **Linux Mint ISO-Datei** (ca. 2–3 GB)

> **Achtung:** Alle Daten auf dem USB-Stick werden beim Erstellen des Bootsticks gelöscht. Vorher sichern!

---

## Schritt 1: Linux Mint ISO herunterladen

1. Öffne im Browser: https://linuxmint.com/download.php
2. Wähle die gewünschte Edition (empfohlen: **Cinnamon**)
3. Klicke auf einen Download-Mirror in deiner Nähe
4. Warte bis die `.iso`-Datei vollständig heruntergeladen ist

---

## Schritt 2: Rufus herunterladen

Rufus ist ein kostenloses Tool zum Erstellen von bootfähigen USB-Sticks.

1. Öffne im Browser: https://rufus.ie
2. Lade die aktuelle Version herunter (z. B. `rufus-4.x.exe`)
3. Keine Installation nötig – einfach die `.exe`-Datei starten

---

## Schritt 3: Bootstick erstellen

1. USB-Stick einstecken
2. Rufus starten (ggf. als Administrator ausführen)
3. Einstellungen in Rufus:

   | Einstellung | Wert |
   |-------------|------|
   | **Laufwerk** | Deinen USB-Stick auswählen |
   | **Startfähiges Laufwerk** | Auf das Ordner-Symbol klicken → Linux Mint `.iso` auswählen |
   | **Partitionsschema** | `GPT` (für neuere PCs mit UEFI) |
   | **Dateisystem** | `FAT32` |

4. Auf **START** klicken
5. Wenn gefragt: **Im ISO-Image-Modus schreiben** auswählen → OK
6. Nochmals bestätigen, dass der USB-Stick überschrieben werden darf
7. Warten bis der Fortschrittsbalken auf **FERTIG** springt (ca. 5–10 Minuten)

---

## Schritt 4: Vom USB-Stick booten

1. Computer neu starten
2. Beim Starten die **Boot-Menü-Taste** drücken (je nach Hersteller unterschiedlich):

   | Hersteller | Taste |
   |------------|-------|
   | Lenovo | F12 |
   | HP | F9 oder Esc |
   | Dell | F12 |
   | ASUS | F8 oder Esc |
   | Acer | F12 |
   | MSI | F11 |

3. Im Boot-Menü den USB-Stick auswählen
4. Linux Mint startet – du kannst es direkt ausprobieren oder installieren

> **Tipp:** Falls kein Boot-Menü erscheint, muss im BIOS/UEFI die Bootreihenfolge geändert werden. Die BIOS-Taste ist meist **Entf**, **F2** oder **F10**.
