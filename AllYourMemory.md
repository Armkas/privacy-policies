# Privacy Policy & Terms of Use for AllYourMemory

**Last Updated: September 16, 2026**

AllYourMemory is developed as a privacy-first, on-device personal memory and notebook application. We believe that your personal thoughts, notes, photos, audio recordings, videos, and files belong exclusively to you.

This document explains our strict data protection practices, the operational architecture of the App, and the terms governing your use of our software.

---

## 1. Core Principle: Zero Personal Data Collection

- **No Remote Servers**: We do not operate any backend servers, databases, user accounts, or cloud processing infrastructure for storing or analyzing your personal data.
- **No Data Transmission**: The App does not collect, track, upload, transmit, share, or sell any of your personal data, notes, images, audio recordings, video files, or search queries.
- **No Third-Party SDKs**: The App contains no third-party analytics SDKs, advertising trackers, telemetry frameworks, or behavioral monitoring tools.
- **Local Sandbox Storage**: All data is saved exclusively inside your device's local application sandbox:
  - **Notes, Tags, and Metadata**: Stored locally in a private database powered by Apple's native SwiftData framework.
  - **Media Attachments**: Original photos, audio recordings, video files, and imported documents are saved directly within the App's sandboxed local `Documents` directory.

---

## 2. Device Permissions and Capabilities

To provide its core functionality, the App may request access to certain iOS capabilities. Each permission is strictly used on-device:

1. **Camera (`NSCameraUsageDescription`)**
   - **Purpose**: Allows you to take photos or record video clips directly into a new memory (e.g., photographing a whiteboard or scanning documents).
   - **Privacy Guarantee**: Photos and videos are saved solely into your local memory storage. Captured images and video frames are analyzed locally using Apple's Vision framework for Optical Character Recognition (OCR) and scene classification. No imagery or extracted text is transmitted off your device.

2. **Microphone (`NSMicrophoneUsageDescription`)**
   - **Purpose**: Enables recording spoken ideas, audio memos, and capturing audio when recording videos.
   - **Privacy Guarantee**: Audio captured via the microphone remains strictly inside the App's local sandbox storage and is never uploaded, streamed, or processed by remote servers.

3. **Speech Recognition (`NSSpeechRecognitionUsageDescription`)**
   - **Purpose**: Transcribes voice memos, imported audio files, and video soundtracks into searchable text with per-sentence timestamps. Before transcription, the spoken language is identified locally.
   - **Privacy Guarantee**: Speech recognition is executed strictly on-device utilizing Apple's Speech framework with mandatory on-device recognition (`requiresOnDeviceRecognition`). Your audio is never sent to remote cloud transcription services.

4. **Photo Library & Media Import (System Photo Picker)**
   - **Purpose**: Allows you to import existing photos and videos into your memories.
   - **Privacy Guarantee**: The App uses Apple's native, out-of-process `PhotosPicker`. The App does not request, possess, or require access to your full Photo Library (`NSPhotoLibraryUsageDescription` is not required). The App only receives access to the specific photos or videos that you explicitly select.

*You can grant or revoke any granted permissions at any time via iOS `Settings > Privacy & Security`.*

---

## 3. Network Access Disclosure (AI Model Downloads)

The App is designed to operate 100% offline for daily note-taking, searching, OCR, and speech transcription.

The **only** network communication initiated by the App occurs when you voluntarily and explicitly choose to download an open-weight local large language model (LLM) from public repositories on Hugging Face (`huggingface.co`).

- **User-Initiated**: The download is an outbound HTTPS request triggered solely when you tap to download a model in `Settings > Local Models`.
- **No Personal Data Sent**: No personal data, notes, transcripts, hardware identifiers, or usage telemetry are transmitted during this request.
- **Third-Party Hosting**: Because the file download connects directly to Hugging Face servers, standard network connection metadata (such as your IP address) is received by Hugging Face to fulfill the file transfer. Downloading model files is subject to [Hugging Face's Privacy Policy](https://huggingface.co/privacy).
- **Offline Inference**: Once downloaded, all model inference (text polishing, translation, and automated tagging) runs 100% offline on your device using the embedded `llama.cpp` inference engine. No network connection is ever required or used during AI processing.

---

## 4. Generative AI & On-Device Language Processing Terms of Use

1. **User Control & Local Processing**:
   - The App provides optional local AI capabilities, including text polishing, language translation, and automatic tag generation.
   - You can enable or disable these automated features at any time in `Settings > AI Assistant` (e.g., toggling automatic tagging, automatic polishing, or translation).
   - When text polishing or translation is applied, the App preserves your original recognized text (`originalContent`), allowing you to revert or view the unmodified text at any time.

2. **No Warranty of Accuracy (AI Output)**:
   - AI outputs are generated through local probabilistic machine learning models without human editorial intervention. Outputs may occasionally contain inaccurate, incomplete, or biased information (hallucinations).
   - The App does not provide medical, legal, financial, or other regulated professional advice. You are solely responsible for reviewing and verifying any AI-suggested content or translations.

3. **Open-Source Model Licenses**:
   - The pre-configured downloadable models are published by their respective creators under permissive or open licenses, as clearly indicated within the App's model catalog:
     - **Qwen3.5 Series** (0.8B, 2B, 4B, 9B): Released by Alibaba Qwen under the **Apache-2.0** license.
     - **LFM2.5 350M**: Released by Liquid AI under the **LFM Open License v1.0** (permitting free use for individuals and commercial organizations with under US$10M annual revenue).
   - Your use of each model is governed by the terms of its respective creator's license.

---

## 5. Data Retention, Backups, and Deletion

- **Data Retention**: Since all data is stored locally on your device, it remains there until you edit or delete it.
- **Deletion**: You can delete individual memories, media attachments, or downloaded models at any time within the App. Deleting the App from your iOS device permanently removes all sandboxed memories, attachments, database records, and downloaded models.
- **System Backups**:
  - **Memories & Attachments**: Your memories and original media files may be included in your standard Apple device backups (such as Apple iCloud Backup or encrypted local computer backups via Finder/iTunes) according to your personal iOS settings. These backups are encrypted and managed entirely by Apple; we have no access to them.
  - **Model Files Excluded**: Downloaded AI model files (which can be several gigabytes in size) are explicitly marked as excluded from backup (`isExcludedFromBackup = true`) to prevent consuming your personal iCloud storage quota. If you restore a backup onto a new device, your memories will be restored, but models will need to be re-downloaded if desired.
  - **No Remote Recovery**: Because we do not operate backend servers, accounts, or cloud copies, we cannot recover or restore your data if your device is lost, stolen, or damaged without an existing Apple device backup.

---

## 6. Children's Privacy

The App does not knowingly collect, solicit, or process any personal information from children under the age of 13 (or the applicable age in your jurisdiction), as the App collects zero personal data from any user.

---

## 7. Changes to This Document

We may periodically update this document to reflect new software capabilities, model offerings, or regulatory requirements. Any updates will be posted to this repository with a revised "Last Updated" date.

---

## 8. Contact Us & Support

If you have any questions, concerns, or feedback regarding this Privacy Policy, your privacy rights, or the App's technical practices, please contact the developer:

- **Email**: [puyue2023@gmail.com](mailto:puyue2023@gmail.com)
- **Repository**: [https://github.com/Armkas/privacy-policies](https://github.com/Armkas/privacy-policies)
