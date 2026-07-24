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
| **📻 Radio** | Browse curated categories — a **Featured** shortlist (WMMR 93.3 Philadelphia, Q104.3 Halifax), Popular, Top Voted, SomaFM, and genres like Rock, Jazz, Lo-fi, Ambient — streamed live from the online directory. |
| **🔎 Search** | Type a station name on the on-screen keyboard to find it. |
| **❤️ Favorites** | Your saved stations, kept between sessions. |
| **📁 Local Files** | Your own music from a USB drive, browsable by album and artist. |
| **🎵 Now Playing** | The current track with its **album art** (or a spinning record when there's none), codec/bitrate, and a live analyzer. |

Pick a station or track and it starts playing. Playback keeps going in the
background while you browse other screens, so hunting for the next song never
cuts the music. In any list, a name too long to fit **scrolls** while it's
highlighted, so the full title is always readable.

On **Now Playing**, a local track shows its **album cover** in a framed square; if
there's no art, a vinyl record spins instead (and stops when paused). The spectrum
bars react to the sound in real time, and `←/→` skip to the previous or next item
from wherever you started listening. When a local track finishes, the **next one
plays automatically** — and with **shuffle** on, the queue plays in a random order.

---

## 🎵 Playing your own music

Jukebox looks for a folder named **`music`** at the **root of a USB drive**, then
scans it (and every sub-folder) and builds a browsable library — grouped by
**Album** and **Artist**, like iTunes.

1. On a computer, open your USB drive.
2. Create a folder named `music` (all lowercase) in the drive's root.
3. Copy your music into it. Sub-folders **are** scanned, so an
   `Artist/Album/track` layout works great.
4. Eject the drive, plug it into the device, and open **Local Files**.

```
USB DRIVE (root)
└── music/
    ├── Daft Punk/
    │   └── Discovery/
    │       ├── 01 One More Time.mp3
    │       └── 02 Aerodynamic.mp3
    └── Bonobo/
        └── Migration/
            └── 01 Migration.flac
```

**Browsing:** Local Files opens to **Albums**, **Artists**, **All Tracks**, or a
**Shuffle** toggle. Pick Albums to see every album (with its artist and track
count), open one, and play a track — `←/→` on Now Playing then steps through that
album, and when it ends the next track starts on its own. Artists drills in the
same way. In the lists, each album/artist shows a colored initial tile; the full
**album cover** appears on Now Playing.

**Album art:** Now Playing shows the cover for the playing track, from either a
cover image in the album folder (`cover.jpg`, `folder.jpg`, or `front.jpg` /
`.png`) or a picture embedded in the file's tags (MP3 `APIC`, FLAC `PICTURE`).
No art? The spinning record shows instead.

**Shuffle:** turn it on from the **Shuffle** row (it shows ON/OFF) or with the
**shoulder buttons** on Now Playing. It's a mode — once on, whatever you play
(an album or All Tracks) runs in random order until you turn it off, and Now
Playing shows **SHUFFLE ON**.

**Where the album/artist names come from:** Jukebox reads the embedded tags —
**ID3v2** in MP3s and **Vorbis comments** in FLAC/OGG (title, artist, album, track
number). For files without tags it falls back to the folder layout: the file's
parent folder becomes the album and the one above it the artist. Anything it
can't place lands under **Unknown Album / Unknown Artist**.

**Supported formats:** `mp3` · `m4a` · `aac` · `flac` · `ogg` · `opus` · `wav` · `wma`
(tag reading covers MP3 and FLAC/OGG; the rest still play and group by folder.)

Seeing *"No music found"*? Make sure the folder is named exactly `music`, sits at
the drive's root, and holds files of the types above. A large library shows
**"Scanning library…"** briefly on first open while tags are read.

---

## On the backglass and DMD

On cabinets with secondary panels (Legends Pinball, 4KP), Jukebox lights them up
too:

- The **backglass** shows the current album cover big — the crisp cover framed
  over a soft, blurred wash of itself, with the track title and artist beneath.
  On radio it shows the station name.
- The **DMD** strip becomes a lit **Jukebox marquee** — the logo on a neon
  gradient, with the track title (or station name) captioned below it.

It updates only when the track changes, so it never affects playback or the
spectrum analyzer. Cabinets without extra panels simply ignore it.

---

## Controls

| Screen | Buttons |
| --- | --- |
| **Menu** | `Arrows` select · `Start` confirm |
| **Radio** | `Arrows` select · `Start` open / play · `Y` favorite · `Back` up a level |
| **Search** | `Arrows` move · `Start` press key · `Back` to menu — then `Start` play, `Y` favorite on results |
| **Favorites** | `Arrows` select · `Start` play · `Y` remove · `Back` to menu |
| **Local Files** | `Arrows` select · `Start` open a list / play a track / toggle Shuffle · `Back` up a level (or to menu at the top) |
| **Now Playing** | `←/→` previous / next · `Start` pause · `L/R shoulder` shuffle · `Y` favorite · `Back` to menu |

---

## Good to know

- **Radio and Search need an internet connection.** Local Files works offline.
- Favorites are saved on the device and survive restarts.
- Radio stations come and go — if one won't play, it may simply be offline; try
  another.
- Auto-advance and shuffle apply to **local files only** — radio streams are
  continuous, so there's nothing to advance to.
- The small version number at the bottom of the main menu (e.g. `v1.0.9`) bumps
  with every build, so you can tell which version is on the device.
