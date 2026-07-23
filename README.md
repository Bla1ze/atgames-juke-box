# 🎛️ Jukebox

A music and internet-radio player for AtGames devices. Browse thousands of online
radio stations, search by name, save your favorites, or play audio files from a
USB drive — with a spinning-vinyl **Now Playing** screen and a live spectrum
analyzer that dances to the music.

Plays MP3, AAC, FLAC, OGG, Opus, WAV, and WMA.

---

## How it works

Open Jukebox and you land on the main menu with five ways to listen:

| | |
| --- | --- |
| **📻 Radio** | Browse curated categories — Popular, Top Voted, SomaFM, and genres like Rock, Jazz, Lo-fi, Ambient — streamed live from the online directory. |
| **🔎 Search** | Type a station name on the on-screen keyboard to find it. |
| **❤️ Favorites** | Your saved stations, kept between sessions. |
| **📁 Local Files** | Your own music from a USB drive. |
| **🎵 Now Playing** | The current track with a spinning record, codec/bitrate, and a live analyzer. |

Pick a station or track and it starts playing. Playback keeps going in the
background while you browse other screens, so hunting for the next song never
cuts the music.

On **Now Playing**, the record spins while audio plays and stops when paused, the
spectrum bars react to the sound in real time, and `←/→` skip to the previous or
next item from wherever you started listening.

---

## 🎵 Playing your own music

Jukebox looks for a folder named **`music`** at the **root of a USB drive**.

1. On a computer, open your USB drive.
2. Create a folder named `music` (all lowercase) in the drive's root.
3. Copy your audio files directly into it — sub-folders aren't scanned.
4. Eject the drive, plug it into the device, and open **Local Files**.

```
USB DRIVE (root)
└── music/
    ├── track-one.mp3
    ├── album-cut.flac
    └── podcast.m4a
```

**Supported formats:** `mp3` · `m4a` · `aac` · `flac` · `ogg` · `opus` · `wav` · `wma`

Seeing *"No music found"*? Make sure the folder is named exactly `music`, sits at
the drive's root, and holds files of the types above.

---

## Controls

| Screen | Buttons |
| --- | --- |
| **Menu** | `Arrows` select · `Start` confirm |
| **Radio** | `Arrows` select · `Start` open / play · `Y` favorite · `Back` up a level |
| **Search** | `Arrows` move · `Start` press key · `Back` to menu — then `Start` play, `Y` favorite on results |
| **Favorites** | `Arrows` select · `Start` play · `Y` remove · `Back` to menu |
| **Local Files** | `Arrows` select · `Start` play · `Back` to menu |
| **Now Playing** | `←/→` previous / next · `Start` pause · `Y` favorite · `Back` to menu |

---

## Good to know

- **Radio and Search need an internet connection.** Local Files works offline.
- Favorites are saved on the device and survive restarts.
- Radio stations come and go — if one won't play, it may simply be offline; try
  another.
