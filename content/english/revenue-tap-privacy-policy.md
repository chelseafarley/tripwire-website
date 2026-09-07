---
title: "Revenue Tap Privacy Policy"
description: "How Revenue Tap handles publisher credentials, on-device analytics data, secure storage, third parties, and advertising."
draft: false
---

**Effective date:** 7 September 2026

Revenue Tap (“the app”) is a local-first publisher analytics app for independent app and web publishers. It is developed by Chelsea Farley.

This policy explains what information the app uses, where it is stored, how sensitive data is protected, and which third parties may receive data when you use the app.

The public copy of this policy is also published at [https://www.tripwiretech.com/revenue-tap-privacy-policy/](https://www.tripwiretech.com/revenue-tap-privacy-policy/).

## Summary

- Your publisher credentials and reporting data are stored **on your device**. Revenue Tap does not operate a cloud account for your analytics.
- Sensitive credentials are stored using the device’s secure storage (iOS Keychain / Android Keystore-backed storage), not in plain text in ordinary app files.
- The app talks directly to Google and Apple services **you** connect, plus a public currency-rate API, and shows ads from Google AdMob.
- You can disconnect a source or delete all local data in Settings at any time.

## Information stored on your device

When you use Revenue Tap, the following may be stored locally:

- **Sign-in credentials** you provide, including Google access tokens and App Store Connect API material (issuer ID, key ID, and `.p8` private key).
- **Reporting data** imported from services you authorize: AdMob, AdSense, Google Analytics 4, Google Play reports, and App Store Connect sales/proceeds. This includes earnings, installs, usage metrics, property names, and related identifiers.
- **Preferences** such as dashboard currency, selected date range, app groupings, and targets.
- **Optional app lock.** If you enable biometric unlock, the app uses the system biometric prompt. Biometric templates stay with the operating system and are not stored by Revenue Tap.

Uninstalling the app typically removes this local data unless you previously exported it.

## How we protect sensitive data

Revenue Tap treats publisher credentials and API keys as sensitive. The app uses the following protection mechanisms:

### Platform secure storage for credentials

Google access tokens, refresh-related credential material, App Store Connect `.p8` private keys, and related connection secrets are stored through the device’s **secure credential store**:

- On **iOS**, values are stored in the system **Keychain**.
- On **Android**, values are stored using **Keystore-backed** encrypted storage.

Credentials are not written as ordinary plain-text files in the app’s documents folder, and they are not copied into the local analytics database used for charts and totals.

### On-device use of App Store Connect keys

Your App Store Connect `.p8` private key remains on the device. The app generates short-lived signed requests (JWTs) **on the device** to call Apple’s APIs. Revenue Tap does not upload the `.p8` key to a Revenue Tap server.

### Separation of credentials and reporting data

Imported reporting metrics (earnings, installs, usage figures, and similar) are stored in a **local on-device database** so the dashboard can work offline. That database is separate from the secure credential store. Credentials used to fetch reports are kept in secure storage as described above.

### Transport security

When the app contacts Google, Apple, Frankfurter, or Google AdMob, it uses **HTTPS** (encrypted transport). Publisher credentials and report requests are not sent to Revenue Tap–operated servers because the app has no such backend for analytics.

### Access controls on the device

- Credentials and local data stay on the device where the app is installed.
- You may enable an optional **biometric app lock** so opening Revenue Tap requires the system Face ID / fingerprint / device credential prompt.
- You can disconnect an account (removing that account’s local credentials and imported rows) or use **Delete all local data** in Settings to wipe credentials and reporting data stored by the app on that device.

### Limits of local storage

No mobile app can guarantee absolute security. Protection depends on your device being up to date, your device passcode/biometrics remaining secure, and the operating system’s Keychain/Keystore features. If someone has unlocked access to your device, they may be able to use apps you have unlocked as well. Revenue Tap does not claim to encrypt reporting rows beyond the protections provided by the operating system for app data.

### Advertising identifiers

On iOS, the app requests **App Tracking Transparency** permission before personalized ad tracking is used. You can decline and still use the app; ads may then be less personalized. You can also limit ad tracking in system settings.

## How the app uses this information

Revenue Tap uses on-device data only to:

- Sign in to the publisher APIs you connect and refresh reports
- Show totals, charts, app breakdowns, targets, and exports
- Convert amounts into your chosen dashboard currency
- Remember your settings

The app does **not** create a Revenue Tap user account, and it does **not** upload your publisher reports or API keys to a Revenue Tap server.

## Network requests and third parties

The app sends requests over the internet to provide its features. Those parties process data under their own policies.

### Google (publisher accounts you connect)

If you connect AdMob, AdSense, Google Analytics, or Google Play, the app uses Google Sign-In and read-only Google APIs (and, for Play, your Cloud Storage reporting bucket). Google receives the authentication and API requests needed to fetch the reports you asked for. Tokens stay on your device.

Google’s policy: [policies.google.com/privacy](https://policies.google.com/privacy)

### Apple (App Store Connect)

If you connect App Store Connect, the app uses your API key on the device to request sales and related reports from Apple. Apple receives those authenticated API requests.

Apple’s policy: [apple.com/legal/privacy](https://www.apple.com/legal/privacy/)

### Currency conversion

To convert store and ad amounts into your dashboard currency, the app requests rates from [Frankfurter](https://www.frankfurter.app/) (ECB-based rates). Requests include currency codes and a date. They do not include your publisher credentials or report rows.

### Advertising (Google AdMob)

Revenue Tap is free and funded by ads. It uses the **Google Mobile Ads** SDK to show banner and interstitial ads.

Google may collect device and advertising information (for example advertising ID, IP address, device type, and coarse location where permitted) to serve and measure ads, including personalized ads where allowed. You can limit ad tracking in your device settings.

- [Google Privacy Policy](https://policies.google.com/privacy)
- [How Google uses data from partners](https://policies.google.com/technologies/partner-sites)
- [AdMob / Google advertising](https://support.google.com/admob/answer/6128543)

### App stores

Apple App Store and Google Play may process install, crash, and (if you opt in) analytics information as part of distributing the app. That processing is governed by Apple and Google, not by Revenue Tap.

## Data we do not sell

We do not sell your personal information. We do not share your publisher reports or API credentials with advertisers or data brokers. AdMob may use device identifiers for advertising as described above.

## Children

Revenue Tap is intended for publishers and developers, not for children under 13 (or the equivalent minimum age in your country). We do not knowingly collect data from children.

## Your choices

In **Settings** you can:

- Disconnect a connected account and remove its local credentials and imported rows
- **Delete all local data**, which clears credentials and reporting data stored by the app on that device
- Export CSV or PDF reports only when you choose to

You can also revoke Google access in your Google account permissions, and revoke or delete App Store Connect API keys in App Store Connect.

## International use

The app runs on your device. Third parties listed above may process data in other countries according to their policies.

## Changes

We may update this policy when the app changes. The effective date at the top will be revised. Continued use after an update means you accept the revised policy.

## Contact

Developer: Chelsea Farley  
App: Revenue Tap  
For any queries contact: chelsea@tripwiretech.com
