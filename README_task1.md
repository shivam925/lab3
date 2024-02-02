# Adding a Home Screen Widget to Your Flutter App

This guide explains how to add a home screen widget (app launcher icon) to your Flutter app using the `flutter_launcher_icons` package.

## **Step 1: Add Dependencies**

Open your `pubspec.yaml` file and add the `flutter_launcher_icons` package as a dependency:

```yaml
dev_dependencies:
  flutter_launcher_icons: ^0.9.2

flutter_icons:
  android: true
  ios: true
  image_path: "assets/icon/app_icon.png"
```

##Step 2: Run Flutter Pub Get
Run the following command in your terminal to fetch the new dependency:
```
flutter pub get
```

##Step 3: Generate Launcher Icons
Run the following command in your terminal to generate the launcher icons:
```
flutter pub run flutter_launcher_icons:main
```
This command will generate the necessary icon files for Android and iOS and update the AndroidManifest.xml and Info.plist files accordingly.

##Step 4: Verify
After running the command, you should see the updated app icon on your device's home screen.

NOTE: The home screen widget is the app icon itself, and Flutter doesn't provide direct support for custom home screen widgets. If you need more complex widgets or interactions on the home screen, consider exploring platform-specific APIs or plugins for Android and iOS.

