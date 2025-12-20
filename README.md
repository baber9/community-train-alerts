# Community Train Alerts

> Simple static web page to receive OneSignal push notifications for train crossing alerts.

## Overview

This repository provides a minimal front-end that initializes OneSignal to deliver push notifications (e.g. "Train approaching", "Train has passed"). The UI is a single `index.html` that displays the community name and requests notification permission from users.

## Features
- Instant browser push notifications via OneSignal
- Lightweight single-file UI (no native app required)

## Files
- `index.html` — main page and OneSignal initialization
- `LICENSE` — project license (MIT)
- `.env` — environment variables (required; not included here)

## Requirements
- Modern web browser with push notification support
- OneSignal account and an App ID

## Environment variables

This project expects environment variables to be provided at build or runtime. Do not commit secrets to the repository. The following variables are used (names only):

- `VITE_ONESIGNAL_APP_ID` — OneSignal App ID used to initialize the SDK
- `VITE_COMMUNITY_NAME` — Friendly name displayed in the UI

Create a `.env` file in the project root containing the variables above when running locally or during your build process. The repository contains a `.env` file locally; its contents are private and should not be shared.

## Running / Preview

Quick preview (uses fallback values unless you inject environment variables):

1. Open `index.html` in your browser.

Recommended (to provide `import.meta.env` variables):

1. Use a toolchain that provides `import.meta.env` (for example, Vite). Create a `.env` with the variables listed above.
2. Serve the site via the chosen toolchain so that `VITE_` variables are injected at build or dev time.

If you prefer a simple replace, you can edit `index.html` and set the `ONESIGNAL_APP_ID` directly, but ensure you do not commit secret keys.

## Contributing

Contributions are welcome. Please open an issue or submit a pull request. Avoid committing sensitive values into `.env` or other files.

## License

This project is licensed under the MIT License — see the `LICENSE` file for details.

## Contact

Repository owner: see project metadata or contact the repository maintainer.
