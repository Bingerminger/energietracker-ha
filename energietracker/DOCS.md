# Energietracker

Energietracker keeps track of your home's energy and water costs: meter
readings in; refund or back-payment, tariff check, notice deadlines and a
forecast out. This app runs the regular Energietracker image
(`ghcr.io/bingerminger/energietracker`) inside Home Assistant and puts it in
the sidebar.

> **New since Energietracker 3.5.0.** The app is marked *experimental* until
> the first reports from Home Assistant OS are in. The program inside is the
> same as in every Docker installation. Feedback is welcome:
> [issues](https://github.com/Bingerminger/energietracker/issues).

Auf Deutsch: [Anleitung im Handbuch](https://github.com/Bingerminger/energietracker/blob/main/docs/anleitungen/home-assistant.md#als-app-in-home-assistant-os).
The complete handbook is also inside the app (**Help**).

## Installation

1. Add the repository `https://github.com/Bingerminger/energietracker-ha`:
   **Settings → Apps → Install app**, menu **⋮ → Repositories**.
2. Install **Energietracker** and start it.
3. Open it from the sidebar (**Energietracker**) or with **Open Web UI**.

**Try with sample data** on the start page shows right away what everything
looks like; your own data is not lost.

## Sign-in

You do not need a separate password. The app takes over the Home Assistant
user who opens it:

- The **first** person to open the app manages the installation; everyone
  after that becomes a **member**. Roles can be changed under
  **Settings → Access**.
- A person is tracked by the Home Assistant user ID. Renaming the user in
  Home Assistant does not create a new person.
- Every Home Assistant user sees the sidebar entry and can open the app.

Only requests that come through Home Assistant's Ingress may name a person.
Everything else (another app, a device on your network) needs a token or an
API key, see below.

## Sending readings from Home Assistant

Home Assistant reaches the app inside its own network, without Ingress. On
the card **Settings → Integrations → 🏠 Home Assistant integration** the app
shows the templates with the right address, which looks like
`http://<host name of the app>/api.php/api/ingest`. Because sign-in is on:

- the push (`rest_command`) needs a **token**; create it on the same card;
- the sensors (balance, forecast) need a **read key**.

The step-by-step guide is in the handbook:
[Connecting Energietracker with Home Assistant](https://github.com/Bingerminger/energietracker/blob/main/docs/en/anleitungen/home-assistant.md).

## Your data and backups

- The data lives in the app's own storage (`/data` inside the container).
  Home Assistant backups include it; restoring such a backup brings it back.
- Inside the app, **Settings → Data → 💾 Backup & restore → Download JSON
  backup** saves everything in one file; snapshots are kept before risky
  steps.
- Sign-in data (persons, token, keys) is not part of the JSON backup, only of
  the Home Assistant backup.

## Moving from a Docker installation

1. In the old installation: **Settings → Data → 💾 Backup & restore →
   Download JSON backup**.
2. In the app: same card, **Import backup…** with that file. Uploads through
   Ingress are streamed, so large backups with receipts work (up to 256 MB).
3. Create a new token (and read key) on the card **🏠 Home Assistant
   integration** and change the address in Home Assistant's `rest_command`
   and sensors to the one the app shows.
4. Stop the old installation once everything is there.

The app must not be older than the installation the backup comes from.

## Direct access (optional)

The port is off by default. If a device outside Home Assistant should reach
the app (a push from another machine, a calendar subscription on your phone),
open the app's **Configuration → Network**, **Show disabled ports** and enter
a free port, for example `8095`. The address is then
`http://<Home Assistant address>:8095`. Without Home Assistant in front, the
app knows no person there: the push needs its token, the calendar link its
key. The interface itself stays in the sidebar.

**Calendar:** under Ingress, **Subscribe in your calendar** shows the address
inside Home Assistant (for Home Assistant's own calendar integration). For a
phone, replace the start of the link up to `/api.php` with the direct
address.

## What is different from a Docker installation

| | App in Home Assistant OS | Docker |
|---|---|---|
| Opening | sidebar (Ingress) | own address and port |
| Sign-in | Home Assistant users, fixed | off, password or proxy, your choice |
| Offline use, install as phone app | no (Home Assistant owns the page) | yes |
| Updates | as an app update in Home Assistant | new image tag |
| Settings via environment | fixed by the app | all `ET_*` variables |
| Logs | **Log** tab of the app | `docker logs` |

The app sets `ET_DATA_DIR=/data`, `ET_AUTH=proxy` and
`ET_TRUSTED_PROXIES=172.30.32.2`. It asks for no access to the Supervisor or
Home Assistant APIs.

## Health and troubleshooting

- The image checks itself (`/api/health`). With **Watchdog** switched on
  (Info tab), Home Assistant restarts the app when that check fails.
- **The app does not start or shows "unhealthy":** look at the **Log** tab.
- **`401` on push:** the token is missing or wrong; create a new one in the
  app.
- **Sensors `unknown`:** read key missing, or the key in the sensor does not
  match the meter.

More in the handbook:
[Troubleshooting](https://github.com/Bingerminger/energietracker/blob/main/docs/en/betrieb/fehlersuche.md).

## License

Energietracker is free software under the GNU Affero General Public License
v3.0 or later, like this app.
