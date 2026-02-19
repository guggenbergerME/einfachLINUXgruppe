# Systemsicherung mit Timeshift unter Linux Mint

---

## Was ist Timeshift?

Timeshift ist ein Programm zur **Systemsicherung** unter Linux.
Es erstellt sogenannte **Snapshots** – Momentaufnahmen des Systemzustands –
und ermöglicht es, das System bei Problemen auf einen früheren Zustand zurückzusetzen.

Timeshift ist unter Linux Mint bereits vorinstalliert.

> **Wichtig:** Timeshift sichert das **Betriebssystem**, nicht deine persönlichen Dateien.
> Für die Sicherung von Dokumenten, Bildern und anderen eigenen Dateien
> braucht man ein separates Backup-Programm (z. B. Déjà Dup).

---

## Wozu brauche ich das?

Typische Situationen, in denen Timeshift hilft:

- Ein Systemupdate hat etwas kaputt gemacht
- Ein installiertes Programm hat das System destabilisiert
- Eine Konfigurationsänderung hat unerwünschte Folgen
- Das System startet nach einer Änderung nicht mehr korrekt

Mit Timeshift kannst du in solchen Fällen das System in wenigen Minuten
auf den letzten funktionierenden Zustand zurücksetzen.

---

## Timeshift starten

### Über das Startmenü

1. Startmenü öffnen
2. Nach **Timeshift** suchen
3. Programm starten (Administratorrechte werden abgefragt)

### Über das Terminal

```bash
sudo timeshift-gtk
```

---

## Erste Einrichtung

Beim ersten Start öffnet sich ein Einrichtungsassistent.

### Schritt 1: Snapshot-Typ wählen

Es gibt zwei Methoden:

| Methode | Beschreibung | Empfehlung |
|---|---|---|
| **RSYNC** | Kopiert Dateien, funktioniert auf jedem Dateisystem | Für die meisten Nutzer |
| **BTRFS** | Nutzt BTRFS-Funktionen, sehr schnell und platzsparend | Nur wenn Festplatte als BTRFS formatiert ist |

**Empfehlung für Linux Mint:** RSYNC wählen

### Schritt 2: Speicherort wählen

- Wähle die Festplatte, auf der die Snapshots gespeichert werden sollen
- Am besten eine **separate Festplatte oder Partition** verwenden
- Snapshots auf der gleichen Partition wie das System sind möglich, aber weniger sicher

### Schritt 3: Zeitplan festlegen

Lege fest, wie oft Timeshift automatisch Snapshots erstellt:

| Intervall | Empfehlung | Aufbewahrung |
|---|---|---|
| Monatlich | Ja | 2 Snapshots |
| Wöchentlich | Ja | 3 Snapshots |
| Täglich | Optional | 5 Snapshots |
| Stündlich | Nein | – |
| Beim Start | Nein | – |

**Empfehlung für Heimanwender:** Wöchentlich + Monatlich aktivieren

### Schritt 4: Benutzerverzeichnisse

Standardmäßig sichert Timeshift **keine** persönlichen Dateien aus `/home`.

- **Keine Auswahl** → nur das System wird gesichert (empfohlen)
- **Versteckte Dateien** → Konfigurationsdateien im Heimverzeichnis werden mitgesichert

---

## Manuellen Snapshot erstellen

Vor wichtigen Änderungen (z. B. System-Update, neue Software) empfiehlt es sich,
einen manuellen Snapshot zu erstellen:

1. Timeshift öffnen
2. Auf **Erstellen** klicken
3. Kurz warten – der Snapshot wird angelegt
4. In der Liste erscheint der neue Eintrag mit Datum und Uhrzeit

### Über das Terminal

```bash
sudo timeshift --create --comments "Vor dem Update"
```

---

## Snapshot wiederherstellen

### Über die grafische Oberfläche

1. Timeshift öffnen
2. Gewünschten Snapshot in der Liste auswählen
3. Auf **Wiederherstellen** klicken
4. Bestätigen – das System wird zurückgesetzt und neu gestartet

### Über das Terminal

```bash
sudo timeshift --restore
```

Es erscheint eine interaktive Auswahl der verfügbaren Snapshots.

---

## Wiederherstellung, wenn Linux nicht mehr startet

Falls das System nach einer Änderung nicht mehr bootet:

1. Linux Mint von einem **USB-Stick** starten (Live-System)
2. Im Live-System Timeshift öffnen
3. Den Speicherort mit den Snapshots angeben
4. Snapshot auswählen und wiederherstellen
5. Computer neu starten

> Tipp: Einen bootfähigen Linux Mint USB-Stick vorbereiten und aufbewahren –
> er ist im Ernstfall unverzichtbar.

---

## Alte Snapshots löschen

Snapshots belegen Speicherplatz. Nicht mehr benötigte Snapshots können gelöscht werden:

1. Timeshift öffnen
2. Snapshot in der Liste auswählen
3. Auf **Löschen** klicken

### Über das Terminal

```bash
sudo timeshift --delete --snapshot '2024-01-15_10-00-00'
```

Alle vorhandenen Snapshots anzeigen:

```bash
sudo timeshift --list
```

---

## Speicherplatzbedarf

Ein typischer Snapshot unter Linux Mint benötigt:

- **Erster Snapshot:** ca. 4–8 GB (vollständige Kopie)
- **Weitere Snapshots:** ca. 300–800 MB (nur Änderungen werden gespeichert)

Empfohlener freier Speicherplatz für Timeshift: **mindestens 20–30 GB**

---

## Zusammenfassung: Empfohlene Einstellungen

| Einstellung | Empfehlung |
|---|---|
| Snapshot-Typ | RSYNC |
| Speicherort | Separate Festplatte oder Partition |
| Zeitplan wöchentlich | Aktiviert, 3 Snapshots aufbewahren |
| Zeitplan monatlich | Aktiviert, 2 Snapshots aufbewahren |
| Heimverzeichnis sichern | Nein (nur System) |
| Vor Updates | Manuellen Snapshot erstellen |

---

## Fazit

Timeshift ist:

- ✔ Einfach zu bedienen
- ✔ Bereits in Linux Mint vorinstalliert
- ✔ Zuverlässiger Schutz vor Systemfehlern
- ✔ Schnelle Wiederherstellung im Problemfall

Einmal eingerichtet, läuft Timeshift automatisch im Hintergrund –
und ist genau dann zur Stelle, wenn man es braucht.
