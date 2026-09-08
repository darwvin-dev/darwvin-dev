# Riso Journal — Privacy Policy

Last updated: September 8, 2026

Riso Journal (`dev.darwvin.risojournal`) is an offline-first Android home-screen personalization app developed by **darwvin-dev**.

## Data collection and sharing

The current release build does not request Internet access, create an account, use advertising, use remote analytics, or use remote crash reporting.

Riso Journal does not transmit the user's tasks, note, theme choices, launcher name, icon setup route, or usage data to the developer or third parties through the app runtime.

## Data stored on the device

Riso Journal stores locally:

- selected palette
- selected wallpaper composition
- three task strings
- task completion state
- one short note
- setup state

Debug/test builds may keep local setup-friction counters. Release builds do not record those tester metrics.

## Permissions and device access

Riso Journal does not request location, contacts, microphone, camera, photos/media, SMS, call log, or broad package-query access.

It uses the normal Android `SET_WALLPAPER` permission only when the user explicitly asks Riso to apply the selected home wallpaper.

The app does not request `QUERY_ALL_PACKAGES`. It can identify the current Android HOME launcher and declares a small explicit allowlist of known launcher/OEM packages only so it can select the correct widget/icon setup route.

## Wallpaper behavior

Riso Journal provides two user-triggered wallpaper paths.

**Quick Setup:** the selected wallpaper is rendered locally on the device and passed directly to Android's `WallpaperManager` for the home screen.

**Preview & Apply:** the selected wallpaper is rendered to a temporary PNG in app cache. Android's wallpaper UI receives temporary read access only to that cached file through a private FileProvider grant.

Riso Journal does not upload generated wallpapers or user content.

## Widgets and icon-pack setup

Riso Journal can ask Android/compatible launchers to pin its own widgets and can open supported launcher or OEM customization routes for its bundled icon pack.

This routing does not grant Riso access to messages, contacts, files, browsing data, accounts, or other private app content.

Some launchers do not expose arbitrary third-party icon-pack application. In those cases Riso shows setup guidance rather than claiming the icons were applied.

## Backups and device transfer

Android app backup is disabled. Explicit backup rules exclude Riso Journal app files, databases, and shared preferences from cloud backup and device-to-device transfer.

## Retention and deletion

Local Riso Journal data remains until the user changes it, uses **Reset Riso Settings**, clears Android app storage, or uninstalls the app.

Temporary preview wallpaper files live in app cache and may be removed by Android or when app storage is cleared.

Resetting Riso Journal settings does not remove a wallpaper that Android has already applied as the system wallpaper.

## Accounts

Riso Journal currently has no account system and therefore no remote account data to delete.

## Google Play

Google Play may independently process information when users install, purchase, or interact with apps through Google Play. Google's processing is controlled by Google and subject to Google's own terms and privacy policies.

If a future Riso Journal release adds Play Billing, remote analytics, crash reporting, ads, cloud services, authentication, or another network service, this policy and the Google Play Data safety declaration will be reviewed before that version is released.

## Privacy inquiries

Developer: **darwvin-dev**

Public privacy inquiry thread:

https://github.com/darwvin-dev/darwvin-dev/issues/1

Please do not post passwords, credentials, private documents, device identifiers, or other sensitive personal information in a public GitHub issue.

## Changes

If Riso Journal's data-handling behavior changes, this policy will be updated before the affected version is distributed.
