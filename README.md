# Google Play services plugins

This project contains plugins to help with using the Google Play services SDK and
the Firebase SDKs for Android.

## Learn more

The plugins contained in this project are meant to work with the following:

- Google Play services SDK: https://developers.google.com/android/guides/overview
- Firebase SDKs for Android: https://firebase.google.com/docs/android/google-services-plugin-and-file

## Contents

### strict-version-matcher-plugin

Helps with managing cross-library version dependencies between components.

### oss-licenses-plugin

Helps apps to display open source software licenses and notices.

### google-services-plugin

_Required for and only for use in apps using Firebase SDKs for Android._

- Converts `google-services.json` into an Android XML resource file (`values.xml`) read by Firebase SDKs at runtime.
- Uses [`strict-version-matcher-plugin`](strict-version-matcher-plugin) to verify that Firebase and Google Play services library dependencies have compatible versions.

For details, see the [Firebase documentation](https://firebase.google.com/docs/android/google-services-plugin-and-file).

## Security & maintenance

### Ratchet

This project uses [Ratchet](https://github.com/sethvargo/ratchet) to ensure all GitHub Actions are pinned to immutable commit SHAs. This helps protect against supply chain attacks by ensuring that the actions used in CI/CD workflows are exactly the versions intended.

Developers are encouraged to run `ratchet pin .github/workflows/*.yml` locally before submitting pull requests that introduce or update GitHub Actions.

