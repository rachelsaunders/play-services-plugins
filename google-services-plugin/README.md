# Google Services (`google-services`) Gradle plugin

The Google services Gradle plugin (`com.google.gms.google-services`) is used with Firebase services and the Firebase Android SDK.

Despite its name, this plugin is specific to Firebase and is distinct from [Google Play services SDKs](https://firebase.google.com/docs/android/learn-more#plugin-vs-google-services-vs-google-play).

The plugin has two main functions:

- **Processes `google-services.json`**: Converts the Firebase configuration values in `google-services.json` into an Android XML resource file (`values.xml`) that Firebase SDKs read at runtime to connect your app to your Firebase project and resources.

- **Checks dependency version compatibility**: Uses [`strict-version-matcher-plugin`](../strict-version-matcher-plugin) to verify that the Firebase and Google Play services libraries in your app have mutually compatible versions.

## Documentation

For setup instructions, configuration options, and details on how the plugin works, see the [Firebase documentation](https://firebase.google.com/docs/android/google-services-plugin-and-file):

* **[Add the Gradle plugin](https://firebase.google.com/docs/android/google-services-plugin-and-file#add-plugin)**: How to add `com.google.gms.google-services` to your Android application (`com.android.application`) or dynamic feature (`com.android.dynamic-feature`) module using the `plugins` DSL (or [legacy `buildscript` syntax](https://firebase.google.com/docs/android/troubleshooting-faq#add-plugins-using-buildscript-syntax)).

* **[Configure the plugin](https://firebase.google.com/docs/android/google-services-plugin-and-file#configure-plugin)**: How to customize plugin behavior using the `googleServices` block (`disableVersionCheck` and `missingGoogleServicesStrategy`).

* **[Add the JSON config file](https://firebase.google.com/docs/android/google-services-plugin-and-file#add-config-file)**: Where to place `google-services.json`, including support for build-type and product-flavor directories.

* **[How the JSON config file is processed](https://firebase.google.com/docs/android/google-services-plugin-and-file#process-config-file)**: How `applicationId` matching works and the complete list of [generated XML string resources](https://firebase.google.com/docs/android/google-services-plugin-and-file#values-in-xml-file) in `values.xml`.

* **[Troubleshooting & FAQ](https://firebase.google.com/docs/android/troubleshooting-faq)**: Solutions for common build and configuration errors (such as `File google-services.json is missing` or `No matching client found for package name`).

* **[Release notes](https://firebase.google.com/support/release-notes/android)**: Latest plugin version and release history.
