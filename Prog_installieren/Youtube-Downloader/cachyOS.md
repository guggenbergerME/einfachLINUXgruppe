# yt-dlp unter CachyOS installieren

## Variante 1: Offizielles Repository (empfohlen)

```bash
sudo pacman -S yt-dlp
```

Test:

```bash
yt-dlp --version
```

Wenn eine Versionsnummer erscheint → läuft

## Variante 2: Mit pip (nur für neueste Git-Version)

```bash
python -m pip install -U yt-dlp
```

> **Hinweis:** Auf Arch/CachyOS ist pacman klar vorzuziehen. pip kann sonst später Probleme mit System-Python verursachen.

---

## ffmpeg installieren (sehr empfohlen)

Für Audio-Extraktion, Merging von Video + Audio usw.:

```bash
sudo pacman -S ffmpeg
```

Test:

```bash
ffmpeg -version
```

---

## Befehle

Video herunterladen:

```bash
yt-dlp https://www.youtube.com/watch?v=VIDEO_ID
```

Beste Qualität (Video + Audio):

```bash
yt-dlp -f bestvideo+bestaudio https://www.youtube.com/watch?v=VIDEO_ID
```

Nur Audio (MP3):

```bash
yt-dlp -x --audio-format mp3 https://www.youtube.com/watch?v=VIDEO_ID
```
