# Mane-Kelsa (ಮನೆ-ಕೆಲಸ) - Final Android Project Guide

This guide will help you build the **Mane-Kelsa** app from scratch. Follow these steps exactly, and you will have a working Android application.

## Step 1: Install Android Studio
1. Go to [developer.android.com/studio](https://developer.android.com/studio).
2. Download and install **Android Studio** (Koala or later recommended).
3. Follow the setup wizard; use the "Standard" settings.

## Step 2: Create the Project
1. Open Android Studio.
2. Click **New Project**.
3. Select **Empty Compose Activity** and click **Next**.
4. Set the following:
   - **Name**: ManeKelsa
   - **Package name**: com.example.manekelsa
   - **Minimum SDK**: API 24 (Android 7.0)
   - **Build configuration language**: Kotlin DSL (build.gradle.kts)
5. Click **Finish**.

## Step 3: Set up Firebase (Real-time Database)
1. Go to the [Firebase Console](https://console.firebase.google.com/).
2. Click **Add project** and name it "ManeKelsa".
3. Add an **Android app** to your Firebase project.
   - For **Android package name**, use `com.example.manekelsa`.
4. Download the `google-services.json` file.
5. In Android Studio, switch the view from "Android" to "Project".
6. Move the `google-services.json` file into the `app` folder.
7. Switch back to the "Android" view.

## Step 4: Add Dependencies
Open `app/build.gradle.kts` and add these in the `dependencies` block:

```kotlin
dependencies {
    // Firebase
    implementation(platform("com.google.firebase:firebase-bom:33.1.0"))
    implementation("com.google.firebase:firebase-database-ktx")
    
    // UI Icons
    implementation("androidx.compose.material:material-icons-extended:1.6.8")
}
```

Add this to the `plugins` block in the same file:
```kotlin
id("com.google.gms.google-services")
```

Open `build.gradle.kts` (Project level) and add this to the `plugins` block:
```kotlin
id("com.google.gms.google-services") version "4.4.2" apply false
```

## Step 5: Localization (100% Kannada)
1. Right-click on `res` folder -> **New** -> **Android Resource Directory**.
2. Select **Locale** from the list, click `>>`.
3. Choose **kn: Kannada**.
4. Right-click the new `values-kn` folder -> **New** -> **Values Resource File**.
5. Name it `strings.xml`. Paste this:

```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">ಮನೆ-ಕೆಲಸ</string>
    <string name="availability_toggle">ನಾನು ಇಂದು ಲಭ್ಯವಿದ್ದೇನೆ</string>
    <string name="call">ಕರೆ ಮಾಡಿ</string>
    <string name="daily_rate">ದೈನಂದಿನ ದರ: ₹%s</string>
    <string name="cleaning">ಮನೆ ಕೆಲಸ</string>
    <string name="gardening">ತೋಟಗಾರಿಕೆ</string>
    <string name="area">ಏರಿಯಾ: %s</string>
    <string name="worker_list_title">ಕೆಲಸಗಾರರ ಪಟ್ಟಿ</string>
</resources>
```

## Step 6: The Full Code
Replace everything in `MainActivity.kt` with the following code.

### [Important] Firebase Database Rules
To ensure the app can read/write during development:
1. In Firebase Console -> Realtime Database -> **Rules**.
2. Change the rules to:
```json
{
  "rules": {
    ".read": "true",
    ".write": "true"
  }
}
```
*(Note: In a real production app, you should secure these, but use this to get started 100% working instantly).*

### [MainActivity.kt Final Code]
Copy the content of `src/MainActivity.kt` and paste it into your `MainActivity.kt` file.

---

## Step 7: Android Manifest (Permissions)
Open `app/src/main/AndroidManifest.xml` and add this line inside the `<manifest>` tag but **outside** the `<application>` tag:

```xml
<uses-permission android:name="android.permission.CALL_PHONE" />
```

## Step 8: Deployment
1. Connect your Android phone via USB.
2. Enable "USB Debugging" in your phone's Developer Options.
3. Click the **Run** button (Green Play icon) in Android Studio.

## Bonus: Import Initial Data
To see workers immediately:
1. In Firebase Console, go to **Realtime Database**.
2. Click the three dots (Data tab) -> **Import JSON**.
3. Upload the `firebase_initial_data.json` provided.

---

### UI Design Principles applied:
- **Large Buttons**: Padding and large font sizes for accessibility.
- **High Contrast**: Yellow/Black or Blue/White color scheme.
- **Call Intent**: Direct integration with the phone dialer.
- **Real-time Search**: Instant filtering by Name or Skill for easier discovery.
- **Real-time Status**: Firebase observers update the UI instantly when a status changes.
