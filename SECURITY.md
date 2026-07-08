```
 ===============================================================================
  PARADIS  ::  SECURITY POLICY
 ===============================================================================
```

## Supported Versions

```
  Release channel     Support window
  -----------------   --------------
  Latest on Releases  Active
  Older APKs          Best-effort only
```

Install only APKs published from this repository's Releases page.

---

## Reporting a Vulnerability

```
  Prefer private disclosure over public GitHub Issues for:
  . Token leakage / credential abuse vectors
  . Remote code risks in update flow
  . Installer / package spoofing concerns
```

Please include:

```
  1. Affected APK version / versionCode (if known)
  2. Device model + Android version
  3. Clear reproduction steps
  4. Impact assessment (what an attacker gains)
  5. Any suggested mitigation
```

Do **not** attach private keys, other users' tokens, or PII dumps.

---

## Scope Boundaries

```
  In scope
  ........ Integrity of Paradis APK distribution
  ........ Issues that allow account / token compromise through the app
  ........ Broken update mechanism that could deliver an unexpected package

  Out of scope (examples)
  ...................... Abuse of third-party stream hosts
  ...................... AniList platform vulnerabilities (report to AniList)
  ...................... Device OEM bugs unrelated to Paradis
```

---

## Maintainer Commitments

```
  . Acknowledge credible reports when possible
  . Prefer fix-forward public releases
  . Rotate compromised secrets out-of-band (never commit secrets here)
```

```
 ===============================================================================
  end of SECURITY  ::  Paradis
 ===============================================================================
```
