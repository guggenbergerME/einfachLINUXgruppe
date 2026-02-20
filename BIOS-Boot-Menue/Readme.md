# BIOS / Boot-Menü – Tastenkombinationen und Einstellungen

Beim Starten des Computers kann man über bestimmte Tasten ins **BIOS/UEFI** oder direkt ins **Boot-Menü** gelangen. Das ist nötig, um z. B. von einem USB-Stick zu booten.

## Tastenkombinationen nach Hersteller

### Notebooks / Laptops

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

### Desktop-PCs / Mainboards

| Hersteller | BIOS/UEFI aufrufen | Boot-Menü |
|---|---|---|
| **ASUS** | Entf oder F2 | F8 |
| **MSI** | Entf | F11 |
| **Gigabyte** | Entf | F12 |
| **ASRock** | F2 oder Entf | F11 |
| **Biostar** | Entf | F9 |
| **Intel** | F2 | F10 |

### Sonstige

| Gerät / System | BIOS/UEFI aufrufen | Boot-Menü |
|---|---|---|
| **Apple Mac (Intel)** | – | Alt/Option (⌥) gedrückt halten |
| **Microsoft Surface** | Lautstärke+ beim Einschalten halten | – |

> **Tipp:** Die Taste muss **sofort nach dem Einschalten** wiederholt gedrückt werden – noch bevor das Betriebssystem startet.

---

## BIOS-Einstellungen zum Booten vom USB-Stick

Wenn der Computer den USB-Stick nicht automatisch erkennt oder nicht davon bootet, müssen im BIOS/UEFI folgende Einstellungen geprüft und ggf. angepasst werden:

### 1. Boot-Reihenfolge ändern

Im BIOS unter dem Menüpunkt **Boot** (oder **Boot Order** / **Boot Priority**) die Reihenfolge so ändern, dass der **USB-Stick vor der Festplatte** steht. Damit versucht der Computer zuerst vom USB-Stick zu starten.

### 2. Secure Boot deaktivieren

**Secure Boot** verhindert das Starten von nicht signierten Betriebssystemen. Für die meisten Linux-Installationen sollte Secure Boot **deaktiviert** werden:

- Im BIOS unter **Security** oder **Boot** den Eintrag **Secure Boot** suchen
- Auf **Disabled** setzen

> **Hinweis:** Linux Mint und Ubuntu unterstützen Secure Boot grundsätzlich. Falls es trotzdem Probleme beim Booten gibt, Secure Boot testweise deaktivieren.

### 3. Boot-Modus: UEFI vs. Legacy (CSM)

Moderne Computer verwenden **UEFI**. Ältere Systeme nutzen das klassische **BIOS (Legacy)**. Der USB-Stick muss zum Boot-Modus passen:

- **UEFI-Modus** (empfohlen für neuere PCs): USB-Stick mit **GPT** erstellt (z. B. in Rufus)
- **Legacy/CSM-Modus** (für ältere PCs): USB-Stick mit **MBR** erstellt

Falls der USB-Stick nicht im Boot-Menü auftaucht, kann es helfen, den jeweils anderen Modus zu aktivieren oder **CSM (Compatibility Support Module)** einzuschalten.

### 4. Fast Boot deaktivieren

Manche BIOS-Versionen haben eine **Fast Boot**-Option, die den Startvorgang beschleunigt, dabei aber USB-Geräte beim Booten überspringt. Falls der USB-Stick nicht erkannt wird:

- Im BIOS unter **Boot** den Eintrag **Fast Boot** suchen
- Auf **Disabled** setzen
