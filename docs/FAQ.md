```
 ===============================================================================
  PARADIS  ::  FAQ
 ===============================================================================
```

## Product

**Q. Is Paradis free?**  
A. Core streaming is designed to remain free. Sponsored placements may appear when configured. Playback itself is not gated behind a paywall.

**Q. Do I need an account?**  
A. AniList sign-in is required for full tracking, list sync, and a proper profile experience.

**Q. Is this the source code repository?**  
A. No. This repository is the public APK release and documentation hub.

---

## Installation

**Q. Will installing from GitHub erase my progress?**  
A. Updates that keep package id `com.paradis.app` and the same signing key preserve local storage.  
Changing package id or signing identity acts like a new app.

**Q. Play Store warning / unknown source?**  
A. Expected for sideloaded APKs. Always download from this repository's Releases.

**Q. Can I install on Android TV?**  
A. Designed primarily for phones/tablets. TV layouts are not guaranteed.

---

## Playback

**Q. Why is a title / episode unavailable?**  
A. Catalog metadata and stream hosts are independent. Metadata may list a show while a stream server is temporarily down.

**Q. Subtitles missing?**  
A. Toggle subtitles in player settings. Some Dub sources may not expose subtitles. Server selection can also change available subtitle tracks.

**Q. Chromecast does nothing?**  
A. Cast requires a build environment with native cast modules. Some development shells (Expo Go) cannot complete casting.

---

## AniList

**Q. Login opens a blank or stuck authorize page**  
A. Confirm Redirect URL settings on the AniList application. Prefer the URI shown inside the app. PIN / paste-token fallbacks may be available in-app.

**Q. Does Paradis modify my AniList list?**  
A. Progress is updated when watching crosses the configured completion threshold. That is intentional for hands-free tracking.

---

## Updates

**Q. How do I know an update is real?**  
A. Prefer Release assets from this repository and the `version.json` downloadUrl that points back at those assets.

**Q. Updater failed mid-download**  
A. Retry on stable Wi-Fi. As a fallback, install the APK manually from Releases.

---

## Privacy & Safety

**Q. Where is my AniList token stored?**  
A. On-device in application storage. Treat a compromised / rooted device accordingly.

**Q. Are comments public?**  
A. Episode comments are shared through the coordination service and visible to other users of the app.

```
 ===============================================================================
  end of FAQ  ::  Paradis
 ===============================================================================
```
