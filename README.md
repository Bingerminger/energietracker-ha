# Energietracker for Home Assistant

**English** · [Deutsch](#deutsch)

This repository brings [Energietracker](https://github.com/Bingerminger/energietracker)
to Home Assistant OS as an app (formerly "add-on"): your home's energy costs
in the sidebar, sign-in with your Home Assistant users, data in Home
Assistant backups.

[![Add the repository to your Home Assistant](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FBingerminger%2Fenergietracker-ha)

Or by hand: **Settings → Apps → Install app**, menu **⋮ → Repositories**, add
`https://github.com/Bingerminger/energietracker-ha`.

## Apps

### [Energietracker](./energietracker)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]

The app runs the regular multi-arch image
`ghcr.io/bingerminger/energietracker`; its version is the Energietracker
release. It is new and marked *experimental* for now; feedback is welcome.
How to use it: [DOCS.md](./energietracker/DOCS.md).

Running Home Assistant without the app store (Container or Core)? Run
Energietracker with Docker next to it:
[Docker guide](https://github.com/Bingerminger/energietracker/blob/main/docs/en/betrieb/docker.md).

Questions and bugs: [issues of the main project](https://github.com/Bingerminger/energietracker/issues).

---

## Deutsch

Dieses Repository bringt den [Energietracker](https://github.com/Bingerminger/energietracker)
als App (früher „Add-on“) in Home Assistant OS: die Energiekosten deines
Zuhauses in der Seitenleiste, Anmeldung mit deinen Home-Assistant-Benutzern,
Daten in den Sicherungen von Home Assistant.

[![Repository in Home Assistant hinzufügen](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2FBingerminger%2Fenergietracker-ha)

Von Hand: unter **Einstellungen → Apps** den App-Store öffnen, im Menü
**⋮ → Repositories** die Adresse
`https://github.com/Bingerminger/energietracker-ha` hinzufügen.

Die App nutzt das normale Image `ghcr.io/bingerminger/energietracker`
(amd64 und arm64), ihre Version ist die Energietracker-Version. Sie ist neu
und vorerst als *experimentell* markiert; Rückmeldungen sind willkommen.
Anleitung: [im Handbuch](https://github.com/Bingerminger/energietracker/blob/main/docs/anleitungen/home-assistant.md#als-app-in-home-assistant-os).
Home Assistant ohne App-Store (Container oder Core)? Dann den Energietracker
mit Docker daneben betreiben:
[Docker-Anleitung](https://github.com/Bingerminger/energietracker/blob/main/docs/betrieb/docker.md).

Fragen und Fehler: [Issues des Hauptprojekts](https://github.com/Bingerminger/energietracker/issues).

## Support · Unterstützen

Energietracker is free and stays free. If it helps you, you can support its
development: [buymeacoffee.com/bingerminger](https://buymeacoffee.com/bingerminger).

Der Energietracker ist kostenlos und bleibt es. Wenn er dir hilft, kannst du
die Weiterentwicklung unterstützen:
[buymeacoffee.com/bingerminger](https://buymeacoffee.com/bingerminger).

## License · Lizenz

GNU Affero General Public License v3.0 or later, like Energietracker itself
([LICENSE](LICENSE)).

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
