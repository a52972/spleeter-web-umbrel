# Audio Tools — Umbrel Community App Store

A community app store for audio tools on umbrelOS.

## Apps

- **Removedor de Voz** — Spleeter Web, a self-hosted interface for separating vocals and instruments from audio tracks.

## Add this store to Umbrel

1. Open the Umbrel App Store.
2. Open the menu beside the search field and choose **Community App Stores**.
3. Add this repository URL: `https://github.com/a52972/spleeter-web-umbrel`
4. Open the new **Audio Tools** store and install **Removedor de Voz**.

## About the app

This package uses the upstream Docker images from [JeffreyCA/spleeter-web](https://github.com/JeffreyCA/spleeter-web). It supports uploads and separation into vocals, accompaniment, bass, and drums, depending on the selected model.

Audio processing runs on the Umbrel host. The first separation can take time because models may need to be downloaded. Performance depends on available RAM, CPU, and storage.

The app is routed through Umbrel's `app_proxy`; it does not bind host ports 80 or 443, so it avoids the port conflict encountered with a standalone nginx deployment.

## Data and backups

Application data is stored below `${APP_DATA_DIR}/data` in separate folders for the database, uploaded/generated media, models, task queue, static assets, and Redis. Back up this directory before uninstalling or making major changes.

## Upstream

- Project: https://github.com/JeffreyCA/spleeter-web
- The upstream project is licensed under MIT. This Umbrel packaging is community-maintained and is not an official Umbrel app.
