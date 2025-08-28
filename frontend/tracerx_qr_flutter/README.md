## Setup Instructions:

### Required Software:
- Flutter SDK: Latest stable version (e.g., 3.24.x). Download from https://flutter.dev/setup.
- Android Studio: Latest version (e.g., 2024.1.x) for Android development and emulators.
- Xcode: Latest version (e.g., 15.x or higher) for iOS development and simulators (macOS only).
- JDK: Java 17+ for Android builds (installed via Android Studio or separately).
- Git: For version control (optional but recommended).

### Step-by-Step Setup:
1. **Install Flutter**: Follow instructions at https://flutter.dev/setup for your OS. Run `flutter doctor` to verify setup.
2. **Set Up Emulators**:
   - Android: Open Android Studio, go to AVD Manager, create a virtual device (e.g., Pixel 6 with API 34).
   - iOS: Open Xcode, go to Window > Devices and Simulators, create a simulator (e.g., iPhone 15).
3. **Create Project**: Create a new Flutter project with `flutter create tracerx_qr`, then replace files with the provided code.
4. **Add Dependencies**: Copy the pubspec.yaml content, then run `flutter pub get` in the project root.
5. **Generate Hive Adapters**: Run `flutter pub run build_runner build` to generate user_model.g.dart.
6. **Run the App**: 
   - For Android: `flutter run` (with emulator running).
   - For iOS: `flutter run` (with simulator running, on macOS).
7. **Build for Release**: `flutter build apk` for Android, `flutter build ios` for iOS.

