# Alternative zur FritzBox mit OPNsense

## (Option A – Fanless Mini-PC Lösung)

---

## Ziel

Wir möchten im privaten Haushalt eine moderne, sichere und unabhängige Router-Lösung aufbauen –
als Alternative zur klassischen FritzBox.

Statt einer „Alles-in-einem-Box" setzen wir auf eine flexible Open-Source-Lösung mit **OPNsense**.

---

## Das Herzstück: Ein kleiner, lüfterloser Mini-PC

Dieser Mini-PC übernimmt die Rolle des Routers und der Firewall.

Er:

- verbindet euer Heimnetz mit dem Internet
- schützt vor unerwünschten Zugriffen
- verwaltet Geräte im Netzwerk
- ermöglicht sicheres VPN von unterwegs
- kann Werbung und Tracker blockieren

Und das Beste:
Er ist **lüfterlos**, leise und stromsparend – perfekt für den Dauerbetrieb im Haushalt.

---

## Wie sieht das Zuhause-Netzwerk damit aus?

Statt einer einzelnen FritzBox sieht es künftig so aus:

```
Internet / Glasfaser
        │
     Mini-PC mit OPNsense
        │
     Netzwerk-Switch
        │
     WLAN Access Point
        │
     Alle Geräte im Haus
```

Das bedeutet:

- Der Mini-PC macht Routing & Sicherheit
- Ein separates WLAN-Gerät sorgt für starkes und stabiles WLAN
- Optional können weitere Geräte ergänzt werden

---

## Warum WLAN separat?

Bei einer FritzBox ist alles in einem Gerät integriert.

Hier trennen wir es bewusst:

- ✔ Router & Sicherheit
- ✔ WLAN

Vorteile:

- Bessere WLAN-Abdeckung
- Erweiterbar (z. B. mehrere Access Points)
- Stabiler Betrieb
- Flexibel austauschbar

---

## Welche Vorteile bringt OPNsense im Alltag?

### Mehr Sicherheit

- Erweiterte Firewall
- Schutz vor Angriffen
- Sichere VPN-Verbindung von unterwegs

### Mehr Kontrolle

- Überblick über alle Geräte im Netzwerk
- Möglichkeit, Gäste-WLAN getrennt zu betreiben
- Optional: eigenes IoT-Netz für Smart-Home Geräte

### Mehr Unabhängigkeit

- Keine Herstellerbindung
- Keine Cloud-Zwangsdienste
- Keine versteckten Einschränkungen

---

## Empfohlene Hardware

Es gibt verschiedene Mini-PCs, die sich gut für OPNsense eignen.
Die wichtigsten Kriterien: **mindestens 2 Netzwerkanschlüsse**, AES-NI-Unterstützung der CPU und möglichst geringer Stromverbrauch.

---

### Einsteiger – bis ca. 150 €

#### Beelink EQ12 / EQ14 (mit USB-Netzwerkkarte)

- Intel N100 / N150 Prozessor (bis 3,4 GHz, 4 Kerne)
- Nur 1 LAN-Port ab Werk → zweiter Port per USB-LAN-Adapter (ca. 15 €) nachrüsten
- 8–16 GB RAM, 256–512 GB SSD
- Lüfter vorhanden (leise), sehr geringer Stromverbrauch (~6–10 W)
- Preisbereich: ca. 100–140 €
- Gut geeignet für einfache Heimnetz-Setups

---

### Mittelklasse – ca. 150–300 €

#### CWWK / MOGINSOK Firewall Appliance (Intel N100 / N150)

- 4 × 2,5 GbE Intel I226-V Netzwerkports (direkt eingebaut)
- Intel N100 oder N150 Prozessor, 4 Kerne, ~6 W TDP
- Lüfterlos (fanless), kompakt
- AES-NI-Unterstützung für VPN
- 8 GB DDR5 RAM + 128 GB NVMe SSD
- Preisbereich: ca. 150–200 €
- Ideal für Heimnetz mit IDS/IPS und VPN

#### Protectli Vault FW4B

- 4 × 1 GbE Intel-Netzwerkports
- Intel Celeron J3160, Quad Core
- Lüfterlos, robustes Gehäuse
- Gut dokumentiert, große Community
- Preisbereich: ca. 220–280 €
- Bewährte Wahl mit langer Supportgeschichte

---

### Leistungsklasse – ab ca. 300 €

#### Protectli Vault V1410 / V1610

- 4–6 × 2,5 GbE Netzwerkports
- Intel N6005 / N6000, bis 3,3 GHz
- 16 GB RAM, 32 GB eMMC (erweiterbar)
- Lüfterlos, sehr kompakt
- Gut für IDS/IPS und mehrere VPN-Tunnel gleichzeitig
- Preisbereich: ca. 350–470 €
- Auch in Deutschland über [eu.protectli.com](https://eu.protectli.com) oder Amazon.de erhältlich

---

### Was ist mit Intel NUC?

Intel NUC-Geräte (Next Unit of Computing) sind ebenfalls als OPNsense-Basis nutzbar:

- Meist nur **1 eingebauter LAN-Port** → zweiter Port per USB-LAN-Adapter nötig
- Leistungsstark (Core i3 / i5 / i7 möglich), aber oft **zu viel Leistung** für einfaches Heimnetz-Routing
- Stromverbrauch höher als spezialisierte Appliances
- Für OPNsense daher **nicht die erste Wahl** – sinnvoll wenn das Gerät schon vorhanden ist

---

### Übersicht auf einen Blick

| Gerät | Ports | Lüfter | Preis ca. | Empfehlung |
|---|---|---|---|---|
| Beelink EQ12/EQ14 | 1 (+USB) | Ja (leise) | 100–140 € | Einstieg |
| CWWK / MOGINSOK N100 | 4 × 2,5 GbE | Nein | 150–200 € | Heimnetz |
| Protectli FW4B | 4 × 1 GbE | Nein | 220–280 € | Bewährt |
| Protectli V1410/V1610 | 4–6 × 2,5 GbE | Nein | 350–470 € | Leistung |
| Intel NUC | 1 (+USB) | Ja | variabel | Bestand |

---

## Stromverbrauch

Ein moderner Mini-PC verbraucht ungefähr so viel wie eine FritzBox.
Die Lösung ist also auch langfristig wirtschaftlich.

---

## Fazit

Die Mini-PC + OPNsense Lösung ist:

- ✔ Modern
- ✔ Sicher
- ✔ Erweiterbar
- ✔ Unabhängig
- ✔ Ideal für technikinteressierte Haushalte

Sie ersetzt eine FritzBox vollständig –
ist aber deutlich flexibler und zukunftssicherer.
