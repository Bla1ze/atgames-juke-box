# Changelog

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
