```
 ===============================================================================
  PARADIS  ::  CHANGELOG
 ===============================================================================
```

All notable public releases are documented in this file.  
Versioning follows SemVer for `latestVersion` and a monotonic integer for `versionCode`.

---

## [Unreleased]

```
  . (none)
```

---

## [2.0.20] - 2026-07-20

```
  versionCode ...... 220

  Added
  ..... Manga mode powered by MangaDex — home feed, genres, search, personal library
  ..... Manga reader with horizontal page & vertical scroll modes
  ..... HD / data-saver image quality, offline page cache, chapter picker, reading progress (expo-sqlite)
  ..... Anime ↔ Manga toggle in app header; dedicated manga bottom tab bar
  ..... Chapter-update checks in foreground (production builds)

  Changed
  ....... Streaming UI polish — #E03C3C accent, Bebas/Outfit/Space Grotesk typography, glass surfaces
  ....... Cast icon centered under notch; sharp anime poster corners preserved
  ....... Manga “Coming Soon” replaced with one-tap switch to manga mode (home & account)
  ....... No ads on manga surfaces (MangaDex AUP)

  Fixed
  ..... Expo Go crash on home tab (expo-notifications guarded import)
  ..... Manga reader settings — page/scroll mode and quality selection apply correctly
```

---

## [2.0.13] - 2026-07-16

```
  versionCode ...... 213

  Fixed
  ..... Production build metadata + public release pipeline sync

  Notes
  ..... New Production Build.
```

---

## [1.1.0] - TBD

```
  versionCode ...... 2 (planned for next public APK publish)

  Added
  ..... Quality / server selection in player settings
  ..... Backend-backed like / dislike counters
  ..... Hardened control lock behavior
  ..... Subtitle safe-area presentation improvements

  Fixed
  ..... Player overlay layout snap artifacts
  ..... Engagement icons cleaned up in landscape bar

  Notes
  ..... Publish this section only when the matching APK is attached to Releases
```

---

## [1.0.0] - Initial public channel

```
  versionCode ...... 1

  Highlights
  .......... First production packaging identity: com.paradis.app
  .......... AniList OAuth-based accounts
  .......... Native episode player with Sub / Dub tracks
  .......... Continue Watching timestamp persistence
  .......... Search with multi-season grouping
  .......... Threaded comments
  .......... Home discovery + My List / Browse tabs
  .......... In-app update plumbing against public version metadata
```

---

## Template for maintainers

```
  ## [X.Y.Z] - YYYY-MM-DD

  versionCode ...... N

  Added
  ..... ...

  Changed
  ....... ...

  Fixed
  ..... ...

  Security
  ........ ...
```

```
 ===============================================================================
  end of CHANGELOG  ::  Paradis
 ===============================================================================
```
