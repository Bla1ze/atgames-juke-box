# Changelog

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
