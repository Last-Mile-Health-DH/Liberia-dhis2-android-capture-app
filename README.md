# DHIS2 Android Capture App

[![Lines of Code](https://sonarcloud.io/api/project_badges/measure?project=dhis2_dhis2-android-capture-app&metric=ncloc)](https://sonarcloud.io/summary/new_code?id=dhis2_dhis2-android-capture-app)
[![Reliability Rating](https://sonarcloud.io/api/project_badges/measure?project=dhis2_dhis2-android-capture-app&metric=reliability_rating)](https://sonarcloud.io/summary/new_code?id=dhis2_dhis2-android-capture-app)

## Introduction

DHIS2 Android Capture App is a mobile application that allows offline data collection for DHIS2. It enables health workers and data collectors to access and update DHIS2 data from their mobile devices without requiring constant internet connectivity.

Main features:

- **Offline-first data capture**. Enter data for events, tracked entities, and data sets without an internet connection. Data is stored locally and synchronized when connectivity is available.
- **Complete DHIS2 workflows**. Support for Tracker programs, Event programs, and Data Sets with validation rules, program rules, and indicators.
- **Native mobile experience**. Built with modern Android technologies to provide a fast, intuitive, and reliable user experience.
- **Synchronized with DHIS2**. Seamlessly integrates with DHIS2 server instances, ensuring data consistency and compatibility across DHIS2 versions.

## Documentation

Implementation guidance and user documentation can be found in the [Android Implementation Guide](https://docs.dhis2.org/en/implement/android-implementation/executive-summary.html) in DHIS2 documentation.

Developer-oriented documentation and architecture details can be found in [AGENTS.md](AGENTS.md).

## Getting Started

This app is built using the [DHIS2 Android SDK](https://github.com/dhis2/dhis2-android-sdk) and the [DHIS2 Mobile UI library](https://developers.dhis2.org/docs/mobile/mobile-ui/overview). To get started with development, check the [AGENTS.md](AGENTS.md) file for comprehensive development guidelines, architecture patterns, and best practices.

## Default server URL

This fork (Last Mile Health / Liberia) pre-fills the server URL field on first launch (when no
accounts are stored on the device yet), so the APK can be distributed to users without asking them
to type or scan the server address.

The default is set in:

```
login/src/commonMain/kotlin/org/dhis2/mobile/login/BrandConfig.kt
```

To change it, update the `DEFAULT_SERVER_URL` constant:

```kotlin
object BrandConfig {
    const val DEFAULT_SERVER_URL = "https://dhis2-liberia.communityhealthacademy.org/"
}
```

Users can still overwrite the pre-filled value or scan a QR code to connect to a different
server — this only sets the initial value shown on a fresh install. Once an account exists on the
device, this default no longer applies.

## Community

Community support can be found in the [DHIS2 Community portal](https://community.dhis2.org/c/implementation/mobile). Any feedback on the app will be highly appreciated.

To report bugs or request new features, visit the [DHIS2 Jira project](https://jira.dhis2.org/projects/ANDROAPP/issues).
