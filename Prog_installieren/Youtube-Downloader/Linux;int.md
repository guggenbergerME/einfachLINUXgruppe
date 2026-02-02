✅ yt-dlp unter Linux Mint installieren
🔹 Variante 1: APT (empfohlen & stabil)

Funktioniert ab Linux Mint 20+.

sudo apt update
sudo apt install yt-dlp

Test:

yt-dlp --version

Wenn eine Versionsnummer kommt → fertig 🎉

🔹 Variante 2: Offizielles Binary (neueste Version)

Falls dir die APT-Version zu alt ist.

sudo wget -O /usr/local/bin/yt-dlp \
https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp


sudo chmod a+rx /usr/local/bin/yt-dlp

Test:

yt-dlp --version

👉 Vorteil: immer topaktuell
👉 Nachteil: Updates manuell

▶️ Erste Nutzung

Video laden:

yt-dlp https://www.youtube.com/watch?v=VIDEO_ID

Beste Qualität:

yt-dlp -f bestvideo+bestaudio https://www.youtube.com/watch?v=VIDEO_ID

Nur Audio (MP3):

yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID