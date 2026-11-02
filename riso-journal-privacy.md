# Riso Journal Privacy Policy

Developer: **darwvin-dev** · App: `dev.darwvin.risojournal` · Last updated: November 2, 2026

Riso Journal is an offline-first Android home-screen personalization and journaling app. Your journal stays on your phone. Riso Circle, an optional social space inside the app, is the only part that uses the Internet, and only if you join it.

## Data collection and sharing

Riso Journal does not use advertising, remote analytics, or remote crash reporting. It never transmits your journal pages, tasks, notes, printed pages, mood ratings you don't post, focus history, launcher information, icon setup routes, or usage data to a server.

## Riso Circle (optional)

Riso Circle lets you post one line a day, share a home-screen look, and follow other people. It is off until you join. Joining uses Google sign-in through Android's Credential Manager; Riso receives a Google ID token, and the Circle server keeps only your Google account's stable identifier (not your email address, contacts, or anything else from your Google account).

When you join, the Circle server (operated by darwvin at circle.darwvin.com) stores: your handle, optional display name and short bio; the posts and setups you choose to share (a line of text, a mood, and a look's world, Studio preset and icon style, never a screenshot); likes, follows, mutes and blocks; reports you make; an invite code and who invited you; and the level, ink score, streak, badge count and number of printed pages shown on your public profile. Other Circle members can see your handle, name, bio, posts, setups, level, ink, streak, badge count and follower count.

Circle data is sent over HTTPS, is not sold, and is not shared with third parties or used for advertising. Reports are reviewed by the developer, who may hide posts or suspend accounts that break the Circle rules.

## Local data

Riso stores the selected palette and wallpaper composition, three task strings and completion state, one short note, printed Daily Print pages with an optional mood rating and highlight, and setup state in app-local storage. Release builds do not record the tester counters used by debuggable development builds.

## Permissions and launcher visibility

Riso does not request broad `QUERY_ALL_PACKAGES` access or sensitive contacts, location, microphone, camera, media, SMS, or call-log permissions.

The normal Android `SET_WALLPAPER` permission is used only when the user explicitly requests wallpaper setup. The app identifies the current HOME launcher and declares a small allowlist of known launcher/OEM setup packages solely to choose the correct widget/icon setup route.

The `INTERNET` permission is used only by Riso Circle. Notifications (`POST_NOTIFICATIONS`) are used for the optional nightly reminder and the Focus 25 timer. Quick Settings tiles act only on your own journal and Focus session.

The Riso Dock widget and Icon Browser read the names of apps you can launch, on the phone only. The Dock also checks which apps are your phone's default dialer, messages, camera, maps, mail, browser and settings, only to pick each app's icon. None of this leaves the phone.

## Wallpaper behavior

**Quick Setup** renders the selected wallpaper locally and passes it to Android's WallpaperManager for the home screen.

**Preview & Apply** renders a temporary PNG in app cache and grants Android's wallpaper UI temporary read access only to that file through a private FileProvider path.

No generated wallpaper or user content is uploaded by Riso Journal.

Exported Daily Print images and monthly PDF collections are saved in app-private storage and leave the device only when you choose a destination in Android's share sheet.

## Riso Premium

Riso Premium is purchased through Google Play, which processes the payment. Riso stores on your device only whether Premium is unlocked, the purchase time, a one-way hash of the purchase token and the date a free trial began, and sends no purchase data anywhere.

## Widgets and icon setup

Riso can request its own App Widgets and can open supported launcher/OEM customization routes for its bundled icon pack. These setup actions do not give Riso access to other apps' private data.

## Backups

Android app backup is disabled. Explicit rules exclude app files, databases, and preferences from cloud backup and device-to-device transfer. You can save a backup file of your journal to a location you pick, and restore from one. Riso never sends it anywhere. You can protect it with a password; without one, anyone with the file can read it, and a forgotten password can't be recovered.

## Reminder and app lock

The optional nightly reminder is a local notification, and needs Android's notification permission once you turn it on. The optional app lock uses Android's biometric prompt; Riso never receives fingerprint or face data.

## Retention and deletion

Local Riso content remains until changed, reset, cleared in Android settings, or the app is uninstalled. Preview PNGs live in cache. Resetting Riso settings does not remove a wallpaper already applied by Android.

## Accounts and deletion

Only Riso Circle has accounts, and they are separate from any darwvin.com account. To delete yours, open Riso Journal → Profile → **Leave Riso Circle**: your account, posts, setups, likes, follows and sessions are deleted from the server immediately. If you no longer have the app, request deletion through the contact below with your Circle handle. Your journal on the phone is never affected.

## Contact

Developer: [darwvin-dev](https://github.com/darwvin-dev).

Privacy inquiries: [public Riso Journal privacy inquiry thread](https://github.com/darwvin-dev/darwvin-dev/issues/1). Do not post credentials, device identifiers, private documents, or other sensitive information in a public issue.
