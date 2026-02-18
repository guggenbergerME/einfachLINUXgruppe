# yt-dlp unter Linux Mint installieren

## Variante 1: APT (empfohlen & stabil)

Funktioniert ab Linux Mint 20+.

```bash
sudo apt update
sudo apt install yt-dlp
```

Test:

```bash
yt-dlp --version
```

Wenn eine Versionsnummer erscheint → fertig

## Variante 2: Offizielles Binary (neueste Version)

Falls die APT-Version zu alt ist:

```bash
sudo wget -O /usr/local/bin/yt-dlp \
https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp

sudo chmod a+rx /usr/local/bin/yt-dlp
```

Test:

```bash
yt-dlp --version
```

Vorteil: immer topaktuell
Nachteil: Updates manuell

---

## Erste Nutzung

Video herunterladen:

```bash
yt-dlp https://www.youtube.com/watch?v=VIDEO_ID
```

Beste Qualität:

```bash
yt-dlp -f bestvideo+bestaudio https://www.youtube.com/watch?v=VIDEO_ID
```

Nur Audio (MP3):

```bash
yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID
```
