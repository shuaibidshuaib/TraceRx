TraceRx QR: Secure Drug/Medicine Verification with Hedera DLT

TraceRx QR is a cutting-edge Flutter mobile application that empowers users to combat counterfeit pharmaceuticals by verifying drug authenticity through QR code scanning, powered by the Hedera Distributed Ledger Technology (DLT). With a sleek interface, seamless API integration, and a gamified rewards system, TraceRx QR ensures transparency in the pharmaceutical supply chain while incentivizing user participation.

 Key Features
QR Code Scanning: Verify drug authenticity by scanning QR codes, retrieving critical details from a secure backend:
Batch ID
Drug Name
Expiry Date
Manufacturer
Token ID


QR Code Generation: Create QR codes for drug batches, enabling secure data sharing (admin access in production).
Fake Drug Reporting: Report suspicious drugs to enhance supply chain integrity, with rewards for community contributions.
Tokenized Incentives: Earn HBAR tokens and achievements (e.g., "First Scan", "5 Day Streak") for verifying and reporting.
User Profiles: Track balance, scan history, reports, and trust score using Hive for persistent storage.
Real-Time Verification: Integrates with a live API (https://tracerx-backend-production.up.railway.app) for instant results.
Engaging UI: Material 3 design with light/dark themes and Lottie animations for a modern, user-friendly experience.

 Technical Stack
Framework: Flutter 3.x (Dart) with Material 3 design
Blockchain: Hedera DLT for secure, tamper-proof verification
Backend: REST API hosted on Railway
Storage: Hive for local user data (balance, scans, achievements)
Key Packages:
mobile_scanner: ^5.1.0 for QR scanning
qr_flutter: ^4.1.0 for QR generation
vibrate: ^0.1.0 for haptic feedback
flutter_spinkit: ^5.2.1 for loading animations
provider: ^6.1.2 for state management
http: ^1.2.2 for API calls
fluttertoast: ^8.2.2 for notifications
lottie: ^3.1.2 for animations


Build Tools: Android Studio, Gradle (NDK 27.0.12077973, Java 11)

 Getting Started
Prerequisites

Flutter SDK: >=3.0.0 <4.0.0
Development Environment: Android Studio or VS Code
Device: Android device/emulator (API 34 recommended)
Git: For cloning the repository

Installation

Clone the Repository:git clone https://github.com/yourusername/tracerx_qr.git
cd tracerx_qr


Install Dependencies:flutter pub get


Set Up Assets:
Create the assets directory:mkdir assets/animations
touch assets/animations/placeholder.txt


Optionally, add Lottie animations (success.json, error.json) from LottieFiles.


Run the App:flutter run

For a release APK:flutter build apk --release
adb install build/app/outputs/flutter-apk/app-release.apk



Configuration

Android Permissions (android/app/src/main/AndroidManifest.xml):<uses-permission android:name="android.permission.CAMERA" />
<uses-feature android:name="android.hardware.camera" android:required="false" />


Build Settings (android/app/build.gradle):android {
    ndkVersion "27.0.12077973"
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_11
        targetCompatibility JavaVersion.VERSION_11
    }
}



 How It Works

Home Screen: Navigate via quick action buttons (Scan QR, Generate QR, Report Fake) or the bottom navigation bar to access features.
Scan QR: Scan a drug’s QR code to verify authenticity via the Hedera-backed API. Valid codes (e.g., RX-2024-001A) display:Verified Drug
Batch ID: RX-2024-001A
Drug Name: Paracetamol
Expiry: 2026-12-31
Manufacturer: PharmaCorp
Token ID: TOKEN-12345

Invalid codes prompt reporting with a "Fake Detected" alert.
Generate QR: Input drug details to create QR codes for batch verification (admin feature).
Report Fake: Submit reports for fake drugs, earning 50 HBAR and updating your trust score.
Rewards & Profile: View HBAR balance, scan/report history, and achievements.

 Testing the App

Sample QR Code: Use QR Code Generator to create a QR code with RX-2024-001A.
API Testing:curl https://tracerx-backend-production.up.railway.app/api/drugs/verify/RX-2024-001A


Emulator: Test on Pixel 6 (API 34) with camera enabled.
Debugging: Run with verbose output:flutter run --verbose



 Real-World Impact
TraceRx QR tackles the global issue of counterfeit drugs, which jeopardize millions of lives annually. By integrating Hedera’s DLT, the app ensures immutable, transparent verification of drug authenticity, fostering trust in the pharmaceutical supply chain. The gamified rewards system encourages user participation, creating a community-driven approach to healthcare safety.

 Future Enhancements
Offline Verification: Cache API responses for offline use.
Multi-Blockchain Support: Integrate with Ethereum or other DLTs.
Analytics Dashboard: Visualize user trust scores and scan trends.
Global Accessibility: Add multi-language support and localization.
