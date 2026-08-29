# PRO FREELANCER AutoReply — minimal debug project

This project intentionally has no Firebase, FCM, billing, AndroidX, Material, or other app libraries. Auto Reply uses the Android Accessibility Service and visible chat controls only.

## Build a debug APK on a PC

1. Open this folder in Android Studio.
2. Allow Android Studio to install the Android SDK 35 platform if it is missing.
3. Build the `app` module with **Build > Build Bundle(s) / APK(s) > Build APK(s)**.
4. The debug APK will be at `app/build/outputs/apk/debug/app-debug.apk`.

## Phone setup

1. Install `app-debug.apk`.
2. Open the app and enter comma-separated keywords and a reply.
3. Turn on Auto Reply and select the target app.
4. Tap **OPEN ACCESSIBILITY SETTINGS** and enable PRO FREELANCER AutoReply.
5. Open the target chat app. The service fills and presses a visible Send control when a configured keyword is visible.

The service does not access private app databases, hidden APIs, or payment/FCM services. The target app must expose an editable message field and a visible Send control through Android Accessibility.