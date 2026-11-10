# Energietracker for Home Assistant

**English** · [Deutsch](#deutsch)

**Energietracker in your Home Assistant sidebar.** Your home's energy costs,
contracts and bills, sign-in with your Home Assistant users, data in Home
Assistant backups.

- **Sensors without YAML:** the integration from the Marketplace or HACS,
  [energietracker-integration](https://github.com/Bingerminger/energietracker-integration)
  creates them.
- **Your AI in the home network (new in 3.12):** an AI program reaches the
  interface only through a port you open under Configuration → Network, not
  through Ingress. Off by default.

This repository brings [Energietracker](https://github.com/Bingerminger/energietracker)
to Home Assistant OS as an app (formerly "add-on").

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

**Der Energietracker in der Seitenleiste von Home Assistant.** Energiekosten,
Verträge und Rechnungen deines Zuhauses, Anmeldung mit deinen
Home-Assistant-Benutzern, Daten in den Sicherungen von Home Assistant.

- **Sensoren ohne YAML:** die Integration aus dem Marketplace oder HACS,
  [energietracker-integration](https://github.com/Bingerminger/energietracker-integration)
  legt sie an.
- **Deine KI im Heimnetz (neu in 3.12):** Ein KI-Programm erreicht die
  Schnittstelle nur über einen Port, den du unter Konfiguration → Netzwerk
  freigibst, nicht über Ingress. Ab Werk aus.

Dieses Repository bringt den [Energietracker](https://github.com/Bingerminger/energietracker)
als App (früher „Add-on“) in Home Assistant OS.

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
