✅ yt-dlp unter CachyOS installieren
🔹 Variante 1: Offizielles Repository (empfohlen)
sudo pacman -S yt-dlp

Test danach:

yt-dlp --version

Wenn eine Versionsnummer kommt → läuft 💪

🔹 Variante 2: Mit pip (nur falls du die neueste Git-Version willst)
python -m pip install -U yt-dlp

⚠️ Hinweis:
Auf Arch/CachyOS ist pacman klar vorzuziehen. pip kann sonst später Ärger mit System-Python machen.

🎬 ffmpeg installieren (sehr empfohlen)

Für Audio-Extraktion, Merging von Video + Audio usw.:

sudo pacman -S ffmpeg

Test:

ffmpeg -version


## Befehle 

Video herunterladen:

yt-dlp https://www.youtube.com/watch?v=VIDEO_ID

Beste Qualität (Video + Audio):

yt-dlp -f bestvideo+bestaudio https://www.youtube.com/watch?v=VIDEO_ID

Nur Audio (MP3):

yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID