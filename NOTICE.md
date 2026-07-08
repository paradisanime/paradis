```
 ===============================================================================
  PARADIS  ::  PUBLIC REPOSITORY NOTICE
 ===============================================================================
```

This repository is the **public distribution and documentation hub** for
Paradis Android APKs.

```
  Contained here
  .............. README, docs, changelog, security / support materials
  .............. version.json for update clients
  .............. GitHub Issue templates
  .............. Release assets (APKs attached to Releases, not committed)

  Not contained here
  .................. Private application source code
  .................. Signing keystores
  .................. Backend secrets / .env files
  .................. Internal architecture blueprints beyond the public overview
```

When creating the remote GitHub repository, set visibility to **Public**.  
Attach APKs only through the Releases UI (or `gh release upload`).

Placeholder values to replace after you create the remote:

```
  YOUR_GITHUB_USERNAME
  YOUR_PUBLIC_REPO
```

Update:

```
  ./version.json          -> downloadUrl
  README / docs links     -> repository URLs if hardcoded later
```

```
 ===============================================================================
```
