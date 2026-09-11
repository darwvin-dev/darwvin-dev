# Riso Journal — Privacy Policy

Last updated: September 11, 2026

Riso Journal (`dev.darwvin.risojournal`) is an offline-first Android home-screen personalization and local daily-journal app developed by **darwvin-dev**.

## Data collection and sharing

The current 0.4.0 release candidate does not request Internet access, create an account, use advertising, use remote analytics, or use remote crash reporting.

Riso Journal does not automatically transmit the user's journal pages, tasks, completion state, note text, focus state, theme choices, launcher name, icon setup route, installed-app coverage information, or usage data to the developer or third parties through the app runtime.

## Data stored on the device

Riso Journal stores locally in app-private storage:

- selected palette and wallpaper composition
- up to three task strings per journal day
- task completion state per journal day
- one short note per journal day
- focus-session end time
- setup and launcher/icon-flow state

Journal History can access locally stored dated entries, and individual journal days can be edited or deleted by the user.

Debug/test builds may keep local setup-friction counters. Non-debuggable release builds do not record those tester metrics.

## Permissions and device access

Riso Journal does not request location, contacts, microphone, camera, photos/media, SMS, call log, or broad package-query access.

It uses the normal Android `SET_WALLPAPER` permission only when the user explicitly asks Riso to apply the selected home wallpaper.

The app does not request `QUERY_ALL_PACKAGES`. Icon Browser uses a narrow `MAIN` + `LAUNCHER` query to read launchable app labels, package names and launcher activity names locally so it can show whether an installed app has a curated Riso mapping. Riso also declares a limited set of launcher/OEM packages only for setup routing.

That installed-app information stays on the device unless the user explicitly chooses **Share icon request**, which opens Android's normal share sheet with the selected app label/package/activity.

## Wallpaper behavior

Riso Journal provides two user-triggered wallpaper paths.

**Quick Setup:** the selected wallpaper is rendered locally on the device and passed directly to Android's `WallpaperManager` for the home screen.

**Preview & Apply:** the selected wallpaper is rendered to a temporary PNG in app cache. Android's wallpaper UI receives temporary read access only to that cached file through a private FileProvider grant.

Riso Journal does not upload generated wallpapers or user content.

## Widgets and icon-pack setup

Riso Journal can ask Android/compatible launchers to pin its own widgets and can open supported launcher or OEM customization routes for its bundled icon pack.

Some launchers expose a direct icon-pack request; others require launcher settings, Samsung Theme Park, or another OEM path. Riso does not report icon success merely because it opened another app or settings screen.

Stock launchers that do not expose a public arbitrary third-party icon-pack API remain Limited. For users who explicitly choose the full icon-pack experience, Riso may open an already-installed compatible launcher or open its public Google Play listing using an Android `ACTION_VIEW` intent. Riso itself still has no Internet permission and does not download the launcher.

This routing does not grant Riso access to messages, contacts, files, browsing data, accounts, or other private app content.

## Journal-page sharing

When the user explicitly chooses **Share page**, Riso renders the selected journal page to a temporary PNG in app cache and sends that file to Android's share sheet through a temporary FileProvider read grant.

Riso does not transmit the image itself. The user chooses the receiving app and destination.

## Backups and device transfer

Android app backup is disabled. Explicit backup rules exclude Riso Journal app files, databases, and shared preferences from cloud backup and device-to-device transfer.

## Retention and deletion

Journal pages and other local app data remain on the device until the user changes or deletes them, clears Android app storage, or uninstalls Riso Journal.

- Individual journal days can be deleted from Journal History.
- **Reset Riso Settings** resets appearance/setup state but deliberately preserves journal pages.
- Clearing Android app storage or uninstalling the app removes app-local journal content.
- Temporary journal-share and wallpaper-preview files live in app cache and may be removed by Android or when app storage is cleared.

Resetting Riso settings does not remove a wallpaper that Android has already applied as the system wallpaper.

## Accounts

Riso Journal currently has no account system and therefore no remote account data to delete.

## Google Play and external apps

Google Play, Galaxy Store, launcher apps, OEM customization tools, and apps selected from Android's share sheet may independently process information when the user interacts with them. Their processing is controlled by those services/apps and is subject to their own terms and privacy policies.

Riso Journal does not receive purchase history or launcher-store account information from those external apps in the current paid-upfront model.

## Future changes

If a future Riso Journal release adds Play Billing inside the app, remote analytics, crash reporting, ads, cloud services, authentication, remote configuration, attribution, or another network service, this policy and the Google Play Data safety declaration will be reviewed before that version is released.

## Privacy inquiries

Developer: **darwvin-dev**

Public privacy inquiry thread:

https://github.com/darwvin-dev/darwvin-dev/issues/1

Please do not post passwords, credentials, private documents, device identifiers, or other sensitive personal information in a public GitHub issue.

## Changes

If Riso Journal's data-handling behavior changes, this policy will be updated before the affected version is distributed.
