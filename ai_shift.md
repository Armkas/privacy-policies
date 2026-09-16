# Privacy Policy & Terms of Service for AI Shift

**Last Updated: September 16, 2026**

AI Shift (AIシフト / 排班神器 / Ca Làm Việc) is developed as a privacy-first, on-device intelligent scheduling application. We firmly believe that your shift schedules, employee records, voice inputs, and business information belong entirely to you.

This document outlines our data protection commitments, technical privacy architecture, and terms governing the use of the App, in strict compliance with the Apple App Store Review Guidelines.

---

## 1. Core Principle: Zero Personal Data Collection

- **No Remote Servers**: We do not operate any backend servers, cloud databases, or remote tracking systems to process or store your schedule or employee data.
- **No Data Transmission**: The App does not collect, track, upload, sell, or transmit any user data, employee names, shift times, notes, or audio inputs to any external server.
- **No Third-Party Trackers**: The App contains no third-party advertising frameworks, behavioral trackers, or analytics SDKs.
- **Local Sandbox Storage**: All shift records, employee profiles, and preferences are stored exclusively on your device within the iOS sandboxed storage (`UserDefaults` and local files).

---

## 2. Device Permissions and Usage

To deliver core features, AI Shift requests access to specific iOS capabilities. Each permission is used solely on-device:

1. **Microphone Access (`NSMicrophoneUsageDescription`)**
   - **Purpose**: Allows you to dictate shift information hands-free using voice input.
   - **Privacy Guarantee**: Audio captured through the microphone is converted to text locally on your device. Your audio is never recorded for telemetry, never stored externally, and never streamed over the network.

2. **Speech Recognition (`NSSpeechRecognitionUsageDescription`)**
   - **Purpose**: Converts spoken schedule descriptions into text for parsing.
   - **Privacy Guarantee**: Speech-to-text processing is performed on-device via Apple's native Speech framework. Your voice data remains private to your device.

*You can grant or revoke any of these permissions at any time in your iOS `Settings > Privacy & Security`.*

---

## 3. Network Access Disclosure (AI Model Weights Download)

AI Shift is designed to run **100% offline** during daily scheduling and AI parsing. 

The **only** network communication initiated by the App occurs when you explicitly choose to download an open-weight local large language model (e.g., Qwen or Gemma GGUF models) from public open-source model repositories (such as `huggingface.co`):
- This network connection is an outbound HTTPS download request purely to fetch public model weights.
- **Zero user data, schedule information, device identifiers, or analytics are transmitted** during this download.
- Once downloaded, the models execute locally on your device via the embedded `llama.cpp` inference engine without requiring any internet connection.

---

## 4. Required System API Disclosures (Privacy Manifest)

In accordance with Apple's Privacy Manifest requirements (`PrivacyInfo.xcprivacy`):
- **UserDefaults (`CA92.1`)**: Used strictly to persist app settings, selected language, onboarding status, and active local model configurations.
- **Disk Space (`E174.1`)**: Used solely to check remaining device storage prior to downloading AI models, preventing system storage exhaustion.
- **Tracking (`NSPrivacyTracking`)**: Set to `false`. We do not track users across apps or websites.

---

## 5. Local Data Sharing & Export (`.aishift`)

- **User-Controlled Sharing**: The App allows you to export schedules as PNG images or `.aishift` files. Such sharing is strictly user-initiated via the native iOS share sheet.
- **Importing Files**: When opening an `.aishift` file, data is imported directly into your device's local database. No cloud intermediate is involved.

---

## 6. Generative AI Disclaimer & Terms of Use

1. **Assisted Parsing**: Natural language shift parsing is conducted by on-device open-source models. The outputs are generated algorithmically.
2. **User Verification**: While the models strive for high accuracy, AI outputs may occasionally contain errors or misinterpretations. You are encouraged to review all parsed shifts before confirming and saving them. The developer is not liable for scheduling conflicts or missed shifts resulting from automated parsing.

---

## 7. Data Retention and Deletion

- **Full User Control**: You maintain complete control over your data.
- **In-App Deletion**: You can delete individual shifts, remove employees, or use the "Clear All Data" button in Settings to purge all records immediately.
- **App Uninstall**: Deleting AI Shift from your device permanently deletes all local shifts, employee lists, and downloaded AI models from your device.

---

## 8. Children's Privacy

AI Shift does not collect, solicit, or share personal data from any person, including children under the age of 13.

---

## 9. Changes to This Policy

We may update this Privacy Policy from time to time to reflect app updates or regulatory requirements. Any revisions will be published to this repository with an updated revision date.

---

## 10. Contact Us & Support

If you have any questions, feedback, or inquiries regarding this Privacy Policy or the App, please contact the developer:

- **Developer**: Armkas
- **Support & Inquiries Email**: puyue2023@gmail.com
