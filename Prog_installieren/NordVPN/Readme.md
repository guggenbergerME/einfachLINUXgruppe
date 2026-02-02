🔐 NordVPN auf Linux Mint installieren
1️⃣ Terminal öffnen

Drück Strg + Alt + T

2️⃣ NordVPN-Repository hinzufügen

Kopier das hier rein und bestätige mit Enter:

curl -sSf https://downloads.nordcdn.com/apps/linux/install.sh | sh

👉 Das Skript richtet alles korrekt ein (Repository, Schlüssel, Paket).

3️⃣ Installation abschließen

Falls es nicht automatisch installiert wurde:

sudo apt update
sudo apt install nordvpn
4️⃣ NordVPN-Dienst starten
sudo systemctl enable nordvpn
sudo systemctl start nordvpn
5️⃣ Bei NordVPN anmelden
nordvpn login

Es öffnet sich ein Browser

Log dich mit deinem NordVPN-Account ein

Danach zurück ins Terminal → fertig ✅

🚀 Verbindung herstellen

Schnell verbinden (empfohlen):

nordvpn connect

Bestimmtes Land wählen (z. B. Deutschland):

nordvpn connect germany

Trennen:

nordvpn disconnect
⚙️ Nützliche Extras (optional, aber nice)

Auto-Connect aktivieren:

nordvpn set autoconnect on

Kill Switch aktivieren (sehr empfohlen):

nordvpn set killswitch on

Status prüfen:

nordvpn status