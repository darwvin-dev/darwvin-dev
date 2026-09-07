# Riso Journal Commercial Build — Privacy Policy Draft

Last updated: September 7, 2026

This policy is prepared for the paid/commercial Riso Journal build that includes Google Play Billing. The currently frozen 0.2.5 usability-validation build is governed by its existing validation privacy policy.

Riso Journal (`dev.darwvin.risojournal`) is an Android home-screen personalization app developed by **darwvin-dev**.

## Local content

Riso Journal stores the following app content locally on the device:

- selected palette
- selected wallpaper composition
- three task strings
- task completion state
- one short note
- setup state
- a local entitlement flag used to remember whether Riso Full is unlocked

Riso does not upload the user's task text, note text, wallpaper choice, or launcher name to a developer server.

## Google Play Billing

The commercial build uses Google Play Billing to sell the one-time digital product `full_unlock`.

Google Play handles the payment flow. Riso Journal does not request or receive the user's raw credit-card number or other raw payment-card credentials.

The app can receive purchase-related information from Google Play that is needed to operate the entitlement, including:

- product ID
- purchase state such as PENDING or PURCHASED
- purchase token / purchase record metadata supplied by the Billing Library
- acknowledgement state

The current commercial branch uses this information on-device to unlock or restore Riso Full and stores only a local entitlement flag for app behavior.

The current commercial branch does not send purchase tokens to a developer-operated backend. If secure server-side purchase verification is added before production, this policy will be updated before that build is distributed.

Google Play independently processes purchase/payment information under Google's terms and privacy policies.

## Other network/data behavior

The current product has:

- no account system
- no advertising SDK
- no remote analytics SDK
- no remote crash-reporting SDK
- no cloud sync
- no location permission
- no contacts permission
- no microphone permission
- no photo/media permission
- no SMS or call-log permission
- no broad package-query permission

Debug/test builds can store local tester counters. Release builds do not record those debug validation counters.

## Launcher access

The app declares narrow visibility for the current Android HOME launcher only so it can display launcher-specific setup guidance. It does not request `QUERY_ALL_PACKAGES`.

## Wallpaper files

When the user asks to apply a wallpaper, Riso Journal generates a temporary PNG in app cache and grants Android's wallpaper UI temporary read access through a private FileProvider path. Older generated Riso wallpaper cache files are removed when a new preview is prepared.

## Backups and device transfer

Android app backup is disabled. Explicit backup rules exclude Riso app files, databases, and shared preferences from cloud backup and device-to-device transfer.

## Retention and deletion

Local Riso data remains until the user changes it, uses **Reset Riso Settings**, clears Android app storage, or uninstalls the app.

A wallpaper already applied by Android remains the system wallpaper until the user changes it.

There is no Riso account and therefore no remote Riso account record to delete.

## Privacy inquiries

Developer: **darwvin-dev**

Public privacy inquiry thread:

https://github.com/darwvin-dev/darwvin-dev/issues/1

Please do not post passwords, payment credentials, private documents, device identifiers, or other sensitive personal information in a public GitHub issue.

## Changes

If the commercial build adds a developer backend, server-side purchase verification, analytics, ads, cloud sync, authentication, or other data handling, this policy will be updated before the affected build is distributed.
