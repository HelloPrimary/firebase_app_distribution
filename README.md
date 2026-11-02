# firebase_app_distribution

This Flutter plugin detects new versions of an app host on Firebase App Distribution.

## Usage

```dart
/// Checks if a new release is available and prompts the user to update
/// if there is one. If user is not signed in as a tester, this method will
/// invite the user to become a tester.
Future<void> updateIfNewReleaseAvailable()

/// Checks if a new release is available.
Future<bool> isNewReleaseAvailable()

/// Checks if tester is signed in.
Future<bool> isTesterSignedIn()

/// Sign in a tester without automatically checking for update.
Future<void> signInTester()

/// Sign out a tester without automatically checking for update.
Future<void> signOutTester()
```

## Android theming

The Firebase App Distribution screens (install / sign-in) use an AppCompat theme provided by the
plugin. To customize it, define a style named `FirebaseAppDistributionTheme` in your app's
`android/app/src/main/res/values/styles.xml`; it must extend a `Theme.AppCompat.*` theme:

```xml
<style name="FirebaseAppDistributionTheme" parent="Theme.AppCompat.DayNight.NoActionBar" />
```

## Contribute

- [ ] Fork the repo
- [ ] Push some changes to your fork
- [ ] In **your own app**, in the `pubspec.yaml` file, point to your fork like this:

```yaml
dependencies:
  ...
  firebase_app_distribution:
    git:
      ref: main
      url: https://github.com/YOUR_GITHUB/firebase_app_distribution.git
```

- [ ] Test your contribution in **your** app
- [ ] Open a pull request with a recording of your test 🙏
