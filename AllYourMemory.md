# Privacy Policy & Terms of Use for AllYourMemory

**Last Updated: September 16, 2026**

AllYourMemory is developed as a privacy-first, on-device personal memory and notebook application. We believe that your personal thoughts, notes, photos, audios, and memories belong exclusively to you. 

This document explains our strict data protection practices, the operational architecture of the App, and the terms governing your use of our software.

---

## 1. Core Principle: Zero Personal Data Collection

- **No Remote Servers**: We do not operate any backend servers, databases, or cloud processing infrastructure for storing your personal notes or files.
- **No Data Transmission**: The App does not collect, track, upload, transmit, share, or sell any of your personal data, memory entries, images, audio recordings, or videos.
- **No Third-Party SDKs**: The App contains no third-party analytics SDKs, advertising trackers, behavioral monitors, or telemetry frameworks.
- **On-Device Storage**: All memories, tags, categories, and media attachments are saved exclusively in your iPhone's local application sandbox storage using Apple's native SwiftData framework.

---

## 2. Device Permissions and Usage

To provide its core functionality, the App may request access to certain iOS capabilities. Each permission is strictly used locally on your device:

1. **Camera (`NSCameraUsageDescription`)**
   - **Purpose**: Allows you to capture photos or short videos directly into your memories (e.g., snapping a photo of a document or whiteboard).
   - **Privacy Guarantee**: Photos and videos are saved solely to your local memory bank. Images are processed locally by Apple's Vision framework to extract readable text (OCR). No imagery or extracted text is transmitted off your device.

2. **Microphone (`NSMicrophoneUsageDescription`)**
   - **Purpose**: Enables recording spoken ideas, audio memos, and voice notes.
   - **Privacy Guarantee**: Audio recordings remain inside the App's local storage and are never uploaded or streamed to external servers.

3. **Speech Recognition (`NSSpeechRecognitionUsageDescription`)**
   - **Purpose**: Transcribes your voice memos into searchable text.
   - **Privacy Guarantee**: Transcription is executed strictly on-device utilizing Apple's native Speech framework with on-device recognition flags. Your voice audio is not sent to remote speech processing services.

*You can grant or revoke any of these permissions at any time via your device's `Settings > Privacy & Security`.*

---

## 3. Network Access Disclosure (Language Model Weights)

The App is designed to operate 100% offline for daily note-taking, searching, OCR, and speech transcription.

The **only** network communication initiated by the App occurs when you explicitly and voluntarily choose to download an open-weight local large language model (e.g., Qwen3.5 GGUF weights) from public repositories such as Hugging Face (`huggingface.co`). 
- This download connection is an outbound HTTPS request solely to retrieve open-source model files.
- **No personal data, memory content, device identifiers, or usage metrics are transmitted during this process.**
- Once a model is downloaded, all text polishing and automated tag generation run completely offline on your device via the embedded `llama.cpp` inference engine.

---

## 4. Generative AI Disclaimer & Terms of Use

1. **Informational & Creative Assistance**: The local text polishing and tagging features utilize open-weight models running on your device. All outputs are generated automatically without human editorial review.
2. **No Warranty of Accuracy**: AI outputs may occasionally produce inaccurate, incomplete, or biased information (hallucinations). The App does not provide medical, legal, financial, or professional advice. You are responsible for reviewing and verifying any AI-suggested text.
3. **Open-Source Licenses**: The pre-configured downloadable model weights are published by their respective authors under permissive open-source licenses (e.g., Apache 2.0). Your use of these models is subject to the terms of their original licenses.

---

## 5. Data Retention, Backups, and Deletion

- **Data Retention**: Since all data is stored locally, it remains on your device until you decide to modify or delete it.
- **Deletion**: You can delete individual memories at any time within the App. Deleting the App from your device permanently removes all locally stored memories, attachments, and downloaded models.
- **Backup Responsibility**: Because we have no cloud copy of your data, you are solely responsible for creating regular backups of your device (e.g., using Apple iCloud Device Backup or encrypted local computer backups). We cannot recover lost data if your device is damaged, lost, or reset.

---

## 6. Children's Privacy

The App does not knowingly collect or solicit any personal information from children under the age of 13 (or under the applicable age in your jurisdiction), as the App collects no personal information whatsoever.

---

## 7. Changes to This Document

We may periodically update this document to reflect new software features or regulatory updates. Any changes will be posted to this repository with an updated revision date.

---

## 8. Contact Us & Support

If you have any questions, concerns, or feedback regarding this Privacy Policy, your privacy rights, or the App's technical practices, please contact the developer at:

- **Email**: [puyue2023@gmail.com]
