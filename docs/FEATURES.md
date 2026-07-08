```
 ===============================================================================
  PARADIS  ::  FEATURE CATALOGUE
 ===============================================================================
```

This document describes product capabilities shipped in production Android builds.  
It is written for users and release reviewers. It does not include private source code.

---

## 1. Discovery & Navigation

```
  Home
  .... Featured hero / carousel content
  .... Curated rows (trending, new, seasonal-style sections)
  .... Continue Watching with precise resume position
  .... Sponsored native placements (when configured)

  Browse
  ...... Genre / catalogue oriented browsing
  ...... Solid dark UI matched to the product design system

  Search
  ...... Live search against AniList metadata
  ...... Filters (genre, year, format, status where exposed)
  ...... Multi-season aggregation so sequels / prequels group sensibly
  ...... Season picker when a title represents a cluster of seasons

  My List
  ....... Local list persistence on device
  ....... AniList collection views when signed in
```

---

## 2. Title Detail

```
  +  Poster / banner presentation
  +  Synopsis, genres, metadata badges
  +  Episode lists with season awareness
  +  Details / comments tab structure
  +  Jump into playback from an episode entry
  +  Add / remove from personal list
```

---

## 3. Playback Experience

```
  Engine
  ...... Native video player (not WebView-based streaming)
  ...... HLS (.m3u8) oriented playback path
  ...... Server / quality selector when multiple sources exist
  ...... Fast server switching while preserving scrub position
  ...... Sub / Dub toggle with millisecond timestamp preserved

  Controls
  ........ Portrait + landscape layouts
  ........ Double-tap seek zones (+/- 10s)
  ........ Seek bar with time labels
  ........ Subtitle toggle and safe-area subtitle rendering
  ........ Fullscreen orientation lock / unlock
  ........ Control lock: hides UI; tap reveals unlock only

  Landscape extras
  ................ Side panels for episodes and comments
  ................ Compact action bar for engagement actions

  Cast
  .... Chromecast picker entry on player overlay
  .... Streams target device when a native cast client is available
  .... Note: casting requires a development / production client with cast
      modules; standard Expo Go may show an unavailable notice
```

---

## 4. Progress, Tracking & Sync

```
  Continue Watching
  ................. Stores episode number + exact second when leaving player
  ................. Home row restores start position via deep resume param

  AniList
  ....... OAuth2 sign-in
  ....... GraphQL progress mutation around high completion milestone (85%)
  ....... Watch status kept in CURRENT while progressing
  ....... Account profile surfaces (avatar / username where available)
```

---

## 5. Engagement & Social

```
  Episode reactions
  ................. Real-time like / dislike counters from backend service
  ................. Per-voter state (like, dislike, or cleared)

  Comments
  ........ Episode-scoped comment threads
  ........ Nested replies
  ........ Publish as authenticated AniList display name when possible

  Notifications
  ............ Local re-engagement nudges after prolonged inactivity
  ............ Highlights unfinished watching / trending-style prompts
```

---

## 6. Monetization (Configured Externally)

```
  Smart link frequency cap
  ...................... At most once per series (not per episode)

  Native sponsored cards
  ..................... Card-shaped placements matching feed geometry
  ..................... "Sponsored" label for clear disclosure

  Notes
  ..... Ad identifiers and scripts are supplied via environment configuration
  ..... Core episode playback remains free and uninterrupted by design
```

---

## 7. Updates & Packaging

```
  Package id .............. com.paradis.app
  Channel ................. GitHub Releases (this public repository)
  In-app updater .......... Compares versionCode; offers APK install intent
  Persistence ............. Same applicationId keeps AsyncStorage / local state
```

---

## 8. Intentional Non-Features (Clarity)

The public release does **not** claim:

```
  - Publishing application source code in this repository
  - Guaranteed availability of every title on every mirror
  - Google Play distribution by default (sideload / Releases based)
  - Perfect cast support inside Expo Go
```

---

## Capability Matrix

```
  Feature                         Status
  -------------------------------- ------------
  AniList login                   Available
  Native HLS player               Available
  Sub / Dub switch                Available
  Quality / server picker         Available
  Control lock                    Available
  Continue Watching               Available
  Season-aware search             Available
  Threaded comments               Available
  Like / dislike                  Available
  Chromecast entrypoint           Available *
  In-app APK update               Available
  -------------------------------- ------------
  * Device / build dependent
```

```
 ===============================================================================
  end of FEATURES  ::  Paradis
 ===============================================================================
```
