# Riso Journal — Privacy Policy

Last updated: September 7, 2026

Riso Journal (`dev.darwvin.risojournal`) is an offline-first Android home-screen personalization app developed by **darwvin-dev**.

## Data collection and sharing

The current release build does not request Internet access, create an account, use advertising, use remote analytics, or use remote crash reporting.

Riso Journal does not transmit the user's tasks, note, theme choices, launcher name, or usage data to the developer or third parties through the app runtime.

## Data stored on the device

Riso Journal stores the following locally on the device for app functionality:

- selected palette
- selected wallpaper composition
- three task strings
- task completion state
- one short note
- setup state

Debug/test builds may keep local setup-friction counters. Release builds do not record those tester metrics.

## Permissions and device access

The current release does not request location, contacts, microphone, camera, photos/media, SMS, call log, or broad package-query access.

The app declares narrow visibility for the current Android HOME launcher only so it can display launcher-specific setup guidance. It does not request `QUERY_ALL_PACKAGES`.

## Backups and device transfer

Android app backup is disabled.

Explicit Android backup rules also exclude Riso Journal app files, databases, and shared preferences from cloud backup and device-to-device transfer.

## Wallpaper files

When the user asks to apply a wallpaper, Riso Journal generates a temporary PNG in app cache and gives Android's wallpaper UI temporary read access to that cached wallpaper through a private FileProvider path.

## Retention and deletion

Local Riso Journal data remains until the user changes it, uses **Reset Riso Settings**, clears Android app storage, or uninstalls the app.

Temporary wallpaper files live in app cache and may be removed by Android or when app storage is cleared.

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
