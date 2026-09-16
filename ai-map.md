# Privacy Policy

**Last Updated:** September 16, 2026

Thank you for using AI Map: Voice GPS Navigation ("AI-MAP", "the App"). This Privacy Policy explains what information the App collects, how it is collected, how it is used, and who it is shared with.

## 1. Summary

* The App works as a normal map without AI. Maps, manual search and navigation do not require sharing data with any AI service.
* AI voice and chat features are powered by third-party AI services: **DeepSeek** and **Google (Gemini API)**.
* **Before any data is sent to a third-party AI service, the App shows a consent screen** explaining what data is sent, who receives it and why. Nothing is sent unless you tap **Agree**.
* You can withdraw consent at any time in **Settings → Privacy → Share data with AI services**. After you withdraw, the App stops sending data to third-party AI services.
* The App does not require an account, and we do not collect your name, email address, phone number or password.

## 2. Information We Collect, How We Collect It and How We Use It

### A. Location Data

* **How it is collected:** From your device's location services, only after you grant location permission in the iOS system prompt.
* **How it is used on your device:** To show your position on the map, search nearby places and provide turn-by-turn navigation using Apple MapKit.
* **Shared with AI services (only with your AI consent):** When you ask an AI question that depends on where you are (for example "coffee nearby" or "weather today"), a text description of your approximate location (such as a place, street or area name) and today's date are sent to Google (Gemini API). While navigating, route details (origin and destination names, waypoints, remaining distance and time) are sent to DeepSeek so that the AI can understand navigation commands. We do not send your continuous location history.

### B. Voice Data (Microphone and Speech Recognition)

* **How it is collected:** Only while you actively use voice features (Push-to-Talk or Continuous mode), after you grant microphone and speech recognition permission in the iOS system prompts.
* **Standard voice:** Speech is transcribed by Apple's Speech framework. Audio processed by Apple is subject to [Apple's Privacy Policy](https://www.apple.com/legal/privacy/).
* **Premium Voice (optional, only with your AI consent):** If you turn on Premium Voice, your voice recording is sent to Google (Gemini API) for transcription.
* The App does not record in the background without an active voice interaction.

### C. Text of Your Requests

* **How it is collected:** From text you type in the AI chat, or text transcribed from your voice.
* **Shared with AI services (only with your AI consent):** The text of your request (limited in length) is sent to DeepSeek to understand it and convert it into map commands. Questions that need real-time or encyclopedic information are sent to Google (Gemini API), which may use Google Search to answer.

### D. Anonymous Identifier, AI Credits and Purchases

* **How it is collected:** The App generates a random anonymous identifier. It is stored in your device Keychain and in your iCloud Key-Value storage so that your AI Credits can be restored on your other devices using the same Apple Account.
* **How it is used:** Our backend (hosted on Supabase) uses this identifier to store your AI Credits balance, verify App Store purchases (transaction identifiers and amounts) and prevent abuse. It is sent to our backend with AI requests for billing, but it is **never forwarded** to DeepSeek or Google. It is not linked to your name, email or Apple Account credentials.
* **Payments:** All purchases are processed by Apple. We never receive your card number, bank information or Apple Account password.

## 3. Who We Share Data With

| Recipient | Data | Purpose |
|---|---|---|
| **DeepSeek** (DeepSeek API) | Text of your requests; navigation details | Understanding requests and generating map commands |
| **Google** (Gemini API) | Real-time questions with approximate location and date; Premium Voice audio | Answering real-time questions; voice transcription |
| **Supabase** (our backend hosting provider) | Anonymous identifier, AI Credits balance, purchase records; AI requests pass through it in transit | Billing, purchase verification and relaying requests to the AI providers above |
| **Apple** (MapKit, Speech, App Store, iCloud) | Location for maps, standard voice transcription, purchases, anonymous identifier sync | Maps, speech recognition, payments, credit restoration |

Data is sent to third-party AI services **only after you give consent in the App**, and only to provide the feature you are using. We do not sell your data and do not use it for advertising.

We only use service providers whose terms provide the same or equal protection of your data as described in this Privacy Policy, and which, under their API terms, do not use API data to train their public models where such an option is offered. Each provider processes data according to its own privacy policy:

* DeepSeek: https://platform.deepseek.com/downloads/DeepSeek%20Open%20Platform%20Privacy%20Policy.html
* Google Gemini API: https://ai.google.dev/gemini-api/terms
* Supabase: https://supabase.com/privacy
* Apple: https://www.apple.com/legal/privacy/

## 4. Data Retention

* We do not store your voice recordings, chat history or location history on our servers. AI requests are relayed to the providers above and are not saved by our backend.
* Third-party AI providers may retain request data temporarily according to their own policies (for example, for abuse monitoring).
* Your anonymous identifier, AI Credits balance and purchase records are kept on our backend for as long as needed to provide credits and meet legal or accounting obligations.
* Settings and preferences are stored locally on your device.

## 5. Your Choices

* **AI data sharing:** Tap **Not Now** on the consent screen, or turn off **Settings → Privacy → Share data with AI services** at any time. The map, manual search and navigation keep working.
* **Permissions:** Location, microphone and speech recognition can be changed at any time in iOS Settings.
* **Deletion requests:** Contact us at the email below to request deletion of data associated with your anonymous identifier.

## 6. Children's Privacy

The App does not knowingly collect personal information from children under 13 (or the minimum age in your jurisdiction). If you believe a child has provided us with personal information, please contact us.

## 7. Data Security

Data is transmitted over encrypted connections (HTTPS/WSS). API keys for AI providers are kept on our backend and never shipped in the App. No method of transmission or storage is completely secure, but we take reasonable measures to protect your information.

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will update the "Last Updated" date above, and for material changes we may notify you in the App.

## 9. Contact Us

**Email:** [puyue2023@gmail.com](mailto:puyue2023@gmail.com)
