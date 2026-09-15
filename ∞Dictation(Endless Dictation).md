# Privacy Policy for ∞Dictation (Endless Dictation)

**Effective Date:** February 11, 2026  
**Last Updated:** September 15, 2026  

Thank you for using **∞Dictation** (also referred to as "Endless Dictation", "∞听写", or "∞文字起こし", hereinafter referred to as the "App"). 

We respect your privacy and are committed to protecting your personal data. This Privacy Policy explains how our App handles your information, what permissions we require, and how third-party services are integrated.

---

## 1. Summary of Core Principles (Local-First Architecture)

* **No User Accounts:** You do not need to register, create an account, or log in to use the App.
* **No Developer Servers:** We do not operate or maintain any backend servers. We do not collect, intercept, store, or sell your personal data.
* **No Analytics or Tracking:** We do not embed any third-party advertising SDKs, tracking frameworks, or behavioral analytics tools. We respect your privacy completely.

---

## 2. Audio Recordings & Voice Data

* **Microphone Access:** To record your voice notes, the App requests permission to access your device’s microphone (`NSMicrophoneUsageDescription`). Recording only occurs when you explicitly initiate it.
* **Local Storage:** All recorded audio and imported media files (audio/video) are stored strictly inside your device’s sandboxed local storage (`Documents` directory).
* **Audio Never Transmitted to Third-Party AI:** Your raw voice recordings are **NEVER uploaded or transmitted to OpenAI, DeepSeek, Google Gemini, or any other external generative AI provider**.

---

## 3. Speech-to-Text Transcription (Apple Speech Framework)

Voice-to-text conversion is performed using **Apple’s native Speech framework (`SFSpeechRecognizer`)**:

* **On-Device Recognition:** When supported by your device and selected language (or when "Force On-Device Recognition" is enabled), transcription is performed 100% locally on your device without transmitting audio over the internet.
* **Server-Assisted Recognition:** If on-device recognition is unavailable for your language, audio is processed by Apple's servers in strict compliance with [Apple’s Privacy Policy](https://www.apple.com/legal/privacy/). We (the App developers) have no access to this process.

---

## 4. Optional AI Post-Processing & "Bring Your Own Key" (BYOK)

The core dictation and transcription functions of the App are entirely functional without any API keys or network connection.

If you choose to use optional AI post-processing features (such as text polishing, summarization, formatting, or translation), the App operates on a **"Bring Your Own Key" (BYOK)** model:

* **Supported AI Providers:** You can configure your own API credentials for providers including **DeepSeek**, **OpenAI**, **Google Gemini**, or a custom OpenAI-compatible endpoint.
* **What Data Is Transmitted:** When you actively trigger an AI action, **only the specific transcribed text snippet** is sent for processing. Raw audio files are never sent.
* **Direct HTTPS Connection:** API requests are transmitted directly and securely from your device to the official endpoint of your chosen provider (e.g., `api.deepseek.com`, `api.openai.com`, or `generativelanguage.googleapis.com`). Requests do not pass through any intermediary or developer-hosted servers.
* **Local Credential Storage:** Your API keys are stored locally on your device in secure application storage (`UserDefaults`). They are used solely to authenticate your direct API requests and are never sent to the developer.
* **Third-Party Privacy Policies:** Data sent to third-party AI providers is subject to their respective terms and privacy policies:
  * [DeepSeek Privacy Policy](https://www.deepseek.com/privacy-policy)
  * [OpenAI Privacy Policy](https://openai.com/policies/privacy-policy)
  * [Google Privacy Policy](https://policies.google.com/privacy)
  *(Official developer APIs typically do not use data submitted via paid/enterprise APIs to train public AI models by default.)*

---

## 5. User Control & Data Retention

* **Data Retention:** Because all data is stored locally on your device, we have no retention period or access to your transcripts.
* **Data Deletion:** You can delete individual transcripts or clear all data at any time via `Settings > Delete All Transcripts`.
* **App Deletion:** Deleting the App from your device permanently removes all locally stored recordings, transcripts, and saved API keys.

---

## 6. Permissions & Consent

* **System Permissions:** You may grant or revoke microphone and speech recognition permissions at any time through iOS `Settings > Privacy & Security`.
* **AI Feature Consent:** Before saving any AI provider configuration, the App presents an explicit disclosure regarding data transmission to the selected provider. You must actively confirm your agreement before the AI features are enabled.

---

## 7. Children's Privacy

The App does not knowingly collect or solicit any personal information from children under the age of 13. Since no personal data is collected or transmitted to external servers managed by us, our App complies with COPPA and relevant child privacy regulations.

---

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in our practices or applicable laws. Any updates will be posted to this page with an updated "Last Updated" date.

---

## 9. Contact Us

If you have any questions, concerns, or requests regarding this Privacy Policy, please contact us at:

* **Developer Email:** puyue2023@gmail.com
