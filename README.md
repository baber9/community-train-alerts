Community Train AlertsA simple, reusable web app for community train crossing notifications using web push (no app install required). Works on Android (automatic) and iPhone (add to Home Screen).Built with OneSignal web push + GitHub Pages. Any community can use it by sharing a custom link.Live Demohttps://baber9.github.io/community-train-alerts/(Change ?community=Your%20Neighborhood in the URL to customize the name.)FeaturesInstant web push notifications when a train is detected.
Subscribe/unsubscribe easily.
Separate statistics dashboard (stats.html) showing:Total trains detected
Trains today
Last train time

Fully static — hosted free on GitHub Pages.
Reusable for any community (custom name via URL parameter).

How It WorksA Python script (running on a local machine/NAS) monitors an RTSP camera audio stream using YAMNet for train horn/rumble detection.
On detection, it sends a push notification via OneSignal API.
Users subscribe via this web page → receive alerts on phone/browser.
Clicking a notification opens the stats dashboard.

Setup for Your CommunityFork this repository.
Enable GitHub Pages (Settings → Pages → Source: main branch /root).
Update OneSignal App ID in the code (or use your own OneSignal app).
Share the link with your neighborhood:

https://yourusername.github.io/your-repo-name/?community=Your%20Neighborhood%20Train%20Alerts

For iPhone UsersOpen the page in Safari.
Tap Share → "Add to Home Screen".
Launch from the Home Screen icon.
Allow notifications when prompted.

For Android UsersOpen in Chrome.
Allow the notification prompt.

UnsubscribingReopen the page.
Use browser settings to block notifications for the site.

Filesindex.html — Subscription page
stats.html — Statistics dashboard
manifest.json — Required for iOS web push
OneSignalSDKWorker.js — Service worker (downloaded from OneSignal)
stats.json — Auto-updated by detector script (example included)

Detector Script (Separate)The Python detection script runs on a local machine with camera access. It:Processes live RTSP audio.
Detects train horns/rumble using YAMNet.
Sends alerts via OneSignal API.
Updates stats.json (committed to repo).

Contact the maintainer for the detector code if needed.CreditsBuilt with  using:OneSignal (web push)
TensorFlow Hub YAMNet (audio classification)
GitHub Pages (hosting)

## For iPhone Users
- Open in Safari.
- Tap Share → "Add to Home Screen".
- Launch from the Home Screen icon.
- Allow notifications when prompted.

## For Android Users
- Open in Chrome.
- Allow the notification prompt.

## Unsubscribing
- **iPhone**: Settings → Safari → Advanced → Website Data → search for your site → Remove. Then delete the Home Screen icon.
- **Android**: Chrome → Settings → Site Settings → Notifications → find site → Block.

You can always re-subscribe by visiting the page again.

## Files
- `index.html` — Subscription page
- `stats.html` — Statistics dashboard
- `manifest.json` — Required for iOS web push
- `OneSignalSDKWorker.js` — Service worker (downloaded from OneSignal)
- `stats.json` — Auto-updated by detector script (example included)

## Detector Script (Separate)
The Python detection script runs on a local machine with camera access. It:
- Processes live RTSP audio.
- Detects train horns/rumble using YAMNet.
- Sends alerts via OneSignal API.
- Updates `stats.json`.

Contact the maintainer for the detector code if needed.

## Credits
Built with ❤️ using:
- OneSignal (web push)
- TensorFlow Hub YAMNet (audio classification)
- GitHub Pages (hosting)

Feel free to fork and adapt for your community! 🚂🔔