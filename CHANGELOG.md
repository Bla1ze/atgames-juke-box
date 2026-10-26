# Changelog

## 2.6 — 26 October 2026

**Plex music, and hold a direction to scroll.**

- **Plex.** Play your Plex Media Server's music. Under **My Music**, choose
  **Plex** (or **USB** for the files on your stick). Link once with the code
  from plex.tv/link on your phone (no typing); Jukebox finds your server and
  remembers it. Browse by artist and album with covers; each track shows its
  own artist. Albums play like local music (queue, next/previous, shuffle,
  favorites). On your home network it connects straight to the server.
- **Hold to scroll.** Hold Up or Down in a list: a short wait, a steady repeat,
  then faster after a second and a half, like Retro Launcher. A held direction
  stops at the top or bottom of a list; a single press still wraps around.
- **What's new before you update.** Updating shows the release notes first, with
  a Not now / Install choice. (It first appears on the update after this one.)
- **Fixed:** after opening the YouTube screen, quitting Jukebox could end in a
  crash instead of a clean exit.

## 2.5 — 19 October 2026

**Surround sound with the SSF kit, a Settings strip, and a sturdier YouTube.**

- **Surround with the SSF kit.** If your cabinet has AtGames' SSF surround kit,
  Jukebox now plays through it automatically. Without the kit, nothing changes:
  stereo as before. Videos and files with real 5.1 sound play in 5.1; stereo
  music is spread across the kit: the front speakers as before, the bass on the
  sub/shaker, and a softer copy without the bass on the rear speakers.
- **Settings.** A new **Settings** strip under the main menu tiles: Surround
  sound (Auto, Off or On), Rear speakers (Off, Low or Medium) and Album covers
  online (On or Off). When an update is available, Settings sits beside the
  update banner.
- **48 kHz playback.** Everything now plays at the cabinet's own rate.
- **Future-proof YouTube.** Jukebox now uses yt-dlp's standalone build, so
  YouTube keeps working after yt-dlp drops the cabinet's older Python. It's a
  one-time 40 MB download, done in the background.
- **Clearer YouTube messages.** Videos that aren't out yet now say "Not out yet:
  premieres in 12 hours"; private and unavailable videos say so too, instead of
  "This cabinet's Python is too old for yt-dlp".
- **A log file, always.** Jukebox writes `jukebox.log` in its own folder (the
  previous session is kept as `jukebox-previous.log`), so problems can be
  reported without editing `jukebox.cfg`. It replaces `jukebox-panels.log` in the
  stick's root, which can be deleted.

## 2.4.4 — 13 October 2026

**Missing album covers are found online.** When a song has no cover in its
folder or inside the file (iTunes Store purchases often kept theirs in iTunes),
Jukebox looks the artist and album up on Apple's iTunes Search and shows the
cover on Now Playing and the backglass. It only takes a cover when the album
name matches exactly, keeps it in `data/covers/` inside the app's folder (never
in your music folders), and asks about each album once. A `cover.jpg` in the
album's folder still wins. `covers = 0` in `/media/usb0/jukebox.cfg` turns the
lookup off.

## 2.4.3 — 13 October 2026

**M4A albums show their covers and names.** Covers built into M4A files now
show on Now Playing and the backglass, with no `cover.jpg` needed. Jukebox also
reads M4A titles, artists, albums and track numbers, so M4A albums are listed
by name and play in track order instead of being grouped by folder.

## 2.4.2 — 7 October 2026

**The backglass now lets go of a video.** After watching YouTube (or a video)
and then playing a song from your library, the backglass could keep showing the
video instead of the song's cover. It now always returns to the cover. Picking
something else while a YouTube video is still starting also can't bring that
video (or its thumbnail) back over the new track.

## 2.4.1 — 7 October 2026

**YouTube covers now show on the cabinet.** In 2.4 the video's thumbnail never
replaced the record on Now Playing: the image step used parts of ffmpeg the
cabinet's copy doesn't have. It now uses only what every ffmpeg has, with
simpler fallbacks, so there's always a cover.

## 2.4 — 7 October 2026

**YouTube on the backglass.**

- **YouTube.** A new YouTube tile: Search YouTube, or pick a music channel —
  Lofi Girl (its 24/7 live radios), NewRetroWave, NoCopyrightSounds and NPR
  Music. A video plays on the backglass like Videos, with Now Playing on the
  playfield; the rest of the list follows, with skip and shuffle. The video's
  thumbnail is the cover (the whole frame, on a soft blur). "Finding the
  stream" shows while it starts, and "Buffering: the stream is slow right now"
  when YouTube sends it slower than it plays.
- **yt-dlp, asked for once.** YouTube plays through yt-dlp (public domain),
  which isn't shipped with Jukebox: the first visit asks, downloads it from
  GitHub (about 3 MB) and keeps it updated weekly.
- **Six tiles.** The main menu is three even rows of two tiles; Videos moved
  from its strip into the grid next to YouTube.
- Emoji in YouTube titles are dropped (the screens' fonts can't draw them).
- The radio LIVE badge is centered, with a steady dot and a soft pulse.

## 2.3 — 7 October 2026

**Videos on the backglass.**

- **Videos.** A new Videos strip on the main menu, under the four tiles, plays
  video files (MP4, M4V, MKV, MOV, WebM, AVI) from a `videos` folder on the USB
  drive, folder by folder. The picture fills the backglass, the playfield shows
  Now Playing with a progress bar, and the DMD shows the title. The rest of the
  folder plays after it, like an album, with skip, pause and shuffle. When it
  ends, the backglass returns to the Jukebox artwork. Placed correctly on both
  the 4KP and the HDP. H.264 up to 1080p30 plays best.
- **Videos over Wi-Fi.** *Add music over Wi-Fi* is now *Add music and videos
  over Wi-Fi*: video files sent from the transfer page go to the `videos`
  folder, keeping their folders.
- The main menu tiles are a little shorter to fit the Videos strip.
- Counts read "1 album", "1 artist" and "1 track" instead of "1 albums".

## 2.2.1 — 6 October 2026

**A small release to try the new in-app updater.** Nothing else changes from
2.2. On 2.2, a banner under the main menu tiles offers this version: select it,
choose Install, then Restart now.

## 2.2 — 6 October 2026

**Add music over Wi-Fi, and updates from inside the app.**

- **Add music over Wi-Fi.** My Music has a new row, *Add music over Wi-Fi*. It
  shows an address and a PIN; open the address in a browser on any computer or
  phone on the same network, and drop in songs or whole artist and album
  folders. They land in the USB drive's `music` folder with their folders kept,
  and the library updates when you close the screen. With no music yet, START
  on the "No music found" screen opens it too.
- **Updates from inside the app.** Jukebox checks for a new version when it
  starts. When there is one, a banner appears under the main menu tiles: select
  it to download and install the update, then restart into it. Only the app is
  replaced; your favorites, your music and the app's picture and description
  are left as they are. This is the first version with the updater, so 2.2
  itself is installed by hand.
- The Favorites tile now says "Save stations with a flipper", matching 2.1.

## 2.1 — 25 September 2026

**Every screen now shows the right thing, on every cabinet.**

- **Fixed the swapped screens on the HDP.** The app used to put its menu on the
  backglass and the backglass artwork on the playfield. Which physical screen is
  which differs by cabinet model, and the app now reads the model to place them
  correctly — playfield, backglass and DMD all land where they belong on both
  the 4KP and the HDP.
- **Favorites no longer need the arcade control panel.** Saving a station was
  bound to `Y`, a button plain cabinets don't have. **A flipper** now saves or
  removes the highlighted station, and favorites the station on Now Playing.
  `Y` still works if you have the panel. Shuffle is unchanged: flippers still
  toggle it during local playback, where there's nothing to favorite.

## 2.0 — 21 September 2026

**A redesigned interface, and a pile of FLAC fixes.**

- **A redesigned interface** — smooth shapes, one type scale, and a button
  legend on every screen.
- **Now Playing takes the album's colours** — the cover fills the background as
  a soft blur, with elapsed and total time on a progress bar.
- **Radio gets a spinning record** with the spectrum radiating around it and a
  pulsing LIVE badge.
- **A new main menu** — a Now Playing card with the current artwork, and tiles
  for Radio, Search, Favorites and My Music.
- **A mini player** on every list, so you can see what's playing while browsing.
- **FLAC album art shows up** — large embedded covers, files carrying an ID3 tag
  in front, and the front cover preferred over a thumbnail. Folder images are
  matched whatever their capitalisation.
- **FLAC tags are read** even when a big picture block sits before them.
- **Every artist is listed.** Artists appearing only on a compilation used to go
  missing, and picking an artist now opens that artist's songs.
- **Albums with the same name stay separate**, `CD1`/`CD2` folders combine into
  one album, and mixed albums show as Various Artists.
- **Lists wrap around**, and long titles scroll on the backglass instead of
  shrinking.
- **Back from Now Playing** returns to My Music when you started there.

## 1.0.14 and earlier

The original release line: merged radio directory, local music browsing by
album and artist, favorites, spinning-vinyl Now Playing with a live spectrum
analyser, and backglass / DMD output.
