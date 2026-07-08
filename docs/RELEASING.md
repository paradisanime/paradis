```
 ===============================================================================
  PARADIS  ::  PUBLIC RELEASE PROCEDURE (MAINTAINERS)
 ===============================================================================
```

This document describes how **maintainers** publish production APKs to the public GitHub release repository.

This repository stores documentation + release metadata.  
APK binaries are attached as GitHub Release assets (preferred). Do not commit large binaries into Git history.

---

## Goals

```
  1. Publish a reproducible, signed APK
  2. Update version metadata for the in-app updater
  3. Write clear release notes for users
  4. Keep package id stable: com.paradis.app
```

---

## Versioning Rules

```
  latestVersion .... human-readable SemVer string (example: 1.1.0)
  versionCode ...... integer, strictly increasing (example: 2, 3, 4...)
  downloadUrl ...... HTTPS URL to the GitHub Release APK asset
  releaseNotes ..... short user-facing summary
```

The in-app updater compares `versionCode` against `Application.nativeBuildVersion`.  
If remote `versionCode` is greater, the client offers an update.

---

## Pre-flight Checklist

```
  [ ] Production APK built and smoke-tested on a physical device
  [ ] Package id is com.paradis.app
  [ ] Signing key matches previous public release (same app update path)
  [ ] AniList login works on the build under test
  [ ] Playback works for a sample title (Sub path at minimum)
  [ ] version.json fields prepared
```

---

## Publish Steps

```
  Step A  -- Create GitHub Release
  .................................
  . Tag format ............... v1.1.0
  . Title .................... Paradis v1.1.0
  . Attach APK .............. paradis.apk (and optional paradis-v1.1.0.apk)
  . Body ..................... paste CHANGELOG section for the version

  Step B  -- Update version.json in this repo
  ...........................................
  {
    "latestVersion": "1.1.0",
    "versionCode": 2,
    "downloadUrl": "https://github.com/<owner>/<public-repo>/releases/download/v1.1.0/paradis.apk",
    "releaseNotes": "Bug fixes and layout stabilization update."
  }

  Step C  -- Commit and push docs / metadata
  ..........................................
  . Update CHANGELOG.md
  . Commit version.json with the Release
  . Verify the downloadUrl opens the APK in a private browser window

  Step D  -- Optional backend mirror
  ..................................
  . If the app fetches version from a CDN / Vercel mirror, sync the same JSON there
```

---

## Asset Naming Convention

```
  Required ........ paradis.apk
  Optional ........ paradis-vMAJOR.MINOR.PATCH.apk
  Forbidden ....... random renames that break documented downloadUrl paths
```

---

## Rollback Notes

```
  . GitHub Releases can be marked as pre-release or unpublished if needed
  . To stop in-app prompts, revert version.json to a lower versionCode only with care:
    clients that already installed a higher versionCode will not "downgrade" automatically
  . Prefer shipping a fix-forward release
```

---

## What Not to Publish Here

```
  x Source code archives of the private app
  x Keystores, passwords, client secrets
  x Internal .env files
  x Unsigned debug APKs labeled as production
```

```
 ===============================================================================
  end of RELEASING  ::  Paradis
 ===============================================================================
```
