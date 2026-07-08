```
 ===============================================================================
  PARADIS  ::  INSTALLATION GUIDE (ANDROID)
 ===============================================================================
```

This guide covers installing production APKs published on GitHub Releases.

---

## Prerequisites

```
  . Android device (phone or tablet)
  . File download ability (browser or GitHub app)
  . Permission to install packages from unknown / new sources
  . Network access for first launch (AniList + catalog)
```

---

## Install from GitHub Releases

```
  Step 1
  ...... Open this repository on GitHub
  ...... Navigate to Releases

  Step 2
  ...... Select the latest stable tag (example: v1.1.0)
  ...... Download the asset named:
            paradis.apk
         or paradis-vX.Y.Z.apk

  Step 3
  ...... Open the downloaded file
  ...... If Android blocks the install, open Settings for that source
         and allow installation of apps

  Step 4
  ...... Confirm install for package id: com.paradis.app
  ...... Launch Paradis and complete AniList sign-in when prompted
```

---

## Update Existing Install

```
  Preferred ........ In-app updater prompt (same package id, keeps local data)
  Manual ........... Download newer APK from Releases and install over previous build

  Important
  ......... Do not change package id between releases.
  ......... Changing package id forces a new app identity and loses local state.
```

---

## First Launch Checklist

```
  [ ] App opens without immediate crash
  [ ] Login / Sign up with AniList succeeds
  [ ] Home feed loads titles
  [ ] Opening a title reaches the detail page
  [ ] Playback starts for at least one episode
  [ ] Continue Watching records position after exit
```

---

## Permissions You May See

```
  Network ............... Required (catalog, streams, auth, comments)
  Notifications ......... Optional (engagement reminders)
  Install packages ...... Required only for in-app update installer
  Nearby devices / Cast . Optional for Chromecast scenarios
```

Exact permission prompts depend on Android version and OEM skins.

---

## Troubleshooting

```
  Install blocked
  ............... Allow this browser / Files app as an install source
  ............... Confirm you downloaded a Release asset, not a random mirror

  App fails to update
  ................... Ensure the new APK is signed with the same release key
  ................... Ensure package id remains com.paradis.app
  ................... Uninstall only as last resort (clears local progress)

  Blank AniList page / login issues
  ................................. Confirm Redirect URL matches what the app shows
  ................................. Use the documented PIN / paste-token fallback if provided
  ................................. Re-open login after clearing a stuck browser tab

  No video
  ........ Check network
  ........ Try Sub / Dub toggle
  ........ Try another server / quality in player settings
  ........ Upstream mirrors can be temporarily unavailable

  Cast unavailable
  ................ Cast needs a build that includes native cast libraries
  ................ Expo Go environments are limited
```

---

## Security Hygiene

```
  . Download APKs only from this repository's Releases page
  . Prefer HTTPS GitHub download links
  . Do not install re-uploaded APKs from unknown Telegram / random sites
  . Keep Android Play Protect / system security settings enabled when possible
```

```
 ===============================================================================
  end of INSTALL  ::  Paradis
 ===============================================================================
```
