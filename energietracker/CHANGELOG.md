# Changelog

The app version is the Energietracker version it runs. What changed in the
program itself is in the
[Energietracker changelog](https://github.com/Bingerminger/energietracker/blob/main/CHANGELOG.en.md).

## 3.9.0

- Runs Energietracker 3.9.0 (`ghcr.io/bingerminger/energietracker:3.9.0`). What changed:
  [release notes](https://github.com/Bingerminger/energietracker/releases/tag/v3.9.0).
- **New permissions:** the app now asks for access to the Home Assistant API, so
  Energietracker can send notifications through the Supervisor (only after you
  switch them on under Settings → Integrations), and for `/share` with write
  access, where it watches the inbox folder `/share/energietracker/posteingang`
  (drop a PDF there, for example through the Samba share app).

## 3.7.0

- Runs Energietracker 3.7.0 (`ghcr.io/bingerminger/energietracker:3.7.0`). What changed:
  [release notes](https://github.com/Bingerminger/energietracker/releases/tag/v3.7.0).

## 3.6.0

- Runs Energietracker 3.6.0 (`ghcr.io/bingerminger/energietracker:3.6.0`). What changed:
  [release notes](https://github.com/Bingerminger/energietracker/releases/tag/v3.6.0).

## 3.5.1

- Runs Energietracker 3.5.1 (`ghcr.io/bingerminger/energietracker:3.5.1`). What changed:
  [release notes](https://github.com/Bingerminger/energietracker/releases/tag/v3.5.1).

## 3.5.0

- First release as a Home Assistant app: sidebar via Ingress, sign-in with
  Home Assistant users, data in the app's storage and in Home Assistant
  backups, direct port off by default.
- Runs the multi-arch image `ghcr.io/bingerminger/energietracker:3.5.0`
  (aarch64, amd64).
