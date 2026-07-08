```
 ===============================================================================
  PARADIS  ::  PRODUCT ARCHITECTURE (PUBLIC)
 ===============================================================================
```

This is a **public**, high-level description of how Paradis works as a product.  
It intentionally omits private source paths, scraper internals, and secrets.

---

## Layer Diagram

```
  +========================================================================+
  |                          Android Client (APK)                          |
  |  UI (dark Crunchyroll-inspired layout)                                 |
  |  Native video player                                                   |
  |  Local progress / list caches                                          |
  |  In-app updater against public Releases                                |
  +-------------------------------+----------------------------------------+
                                  |
                 +----------------+----------------+
                 |                                 |
                 v                                 v
  +---------------------------+     +-------------------------------+
  | AniList GraphQL / OAuth   |     | Lightweight coordination API  |
  | Catalog metadata          |     | Comments + engagement votes   |
  | Watchlist mutations       |     | Health + token exchange helpers|
  +---------------------------+     +-------------------------------+
                 |
                 v
  +------------------------------------------------------------------+
  | Device-side stream resolution against upstream providers         |
  | (user device IP; no central video proxy required for scraping)   |
  +------------------------------------------------------------------+
```

---

## Responsibilities

```
  Mobile client
  ............. Rendering, gestures, playback, local caching
  ............. AniList session storage (device)
  ............. Stream extraction network calls from the device
  ............. APK update download + install intent

  Coordination backend
  .................... Comments storage (MongoDB)
  .................... Episode like / dislike accounting
  .................... Optional OAuth code exchange helper
  .................... Static version.json mirroring (optional)

  AniList
  ....... Identity provider for accounts
  ....... Official anime metadata + list mutation surface

  Public GitHub repo (this project)
  ................................. APK distribution + docs
  ................................. Canonical release notes for users
```

---

## Design Principles

```
  1. Native playback first
  2. Auth via AniList, not custom passwords for watch progress sync
  3. Keep central servers small and free-tier friendly
  4. Prefer clear dark solid UI over experimental visual themes
  5. Ship updates as signed APK over the same package id
```

---

## Data Flow: Watching an Episode

```
  Select title
      |
      v
  Open detail / episode list
      |
      v
  Resolve stream sources on-device
      |
      v
  Native player starts
      |
      +--> Persist local continue-watching timestamp
      |
      +--> On high completion ratio, mutate AniList progress
      |
      +--> Comments / reactions via coordination API
```

---

## Update Flow

```
  Boot
   |
   v
  Fetch version.json (public URL)
   |
   v
  Compare versionCode
   |
   +-- no update --> continue
   |
   +-- update --> download APK from GitHub Releases
                    |
                    v
                  Android package installer (same applicationId)
```

---

## Trust Boundaries

```
  Public release repo ........ binaries + docs only
  Private app repo ........... application source (not published here)
  Backend env ................ secrets never committed
  Device storage ............. tokens / progress kept local to the user device
```

```
 ===============================================================================
  end of ARCHITECTURE  ::  Paradis (public)
 ===============================================================================
```
