# Privacy Policy for Fluffy Drift

**Effective Date:** November 22, 2026  
**Last Updated:** November 22, 2026  
**Application Name:** Fluffy Drift  
**Package / Application ID:** `com.playsphere.fluffydrift`  
**Developer / Publisher:** PlaySphere  
**Contact Email:** [allgames9e@gmail.com](mailto:allgames9e@gmail.com)  

---

## 1. Introduction

Welcome to **Fluffy Drift** ("the Game", "the App", "we", "our", or "us"). We respect your privacy and are committed to protecting any information associated with your use of our mobile and web applications.

This Privacy Policy describes in detail:
- What information we collect, process, and store when you download, install, play, or interact with Fluffy Drift;
- The legal bases and specific purposes for collecting and processing such data;
- How third-party services and Software Development Kits (SDKs) handle data;
- How we safeguard your data and how long it is retained;
- Your rights under international data protection laws, including the **General Data Protection Regulation (GDPR)**, the **California Consumer Privacy Act / California Privacy Rights Act (CCPA/CPRA)**, the **Children's Online Privacy Protection Act (COPPA)**, and the **Google Play Developer Policy**;
- How you can contact us regarding privacy inquiries or request data deletion.

Please read this Privacy Policy thoroughly. By downloading, accessing, or playing Fluffy Drift, you acknowledge that you have read and understood this Privacy Policy. If you do not agree with any part of this policy, please do not install or use the application.

---

## 2. Summary of Key Principles

| Category | Policy Summary |
| :--- | :--- |
| **Personal Identifiable Information (PII)** | We **do not** collect real names, home addresses, phone numbers, contact books, biometric data, or precise GPS location. |
| **Player Identifiers** | An anonymous, pseudonymous device ID (`dev_...`) and optional customizable nickname (e.g., `Drifter #1234`) are generated to support leaderboard rankings and save progress. |
| **Monetization & Ads** | We use **Google AdMob** to display Banner, Interstitial, App Open, and Rewarded ads. AdMob may process device advertising IDs and diagnostic telemetry subject to your consent. |
| **Backend & Cloud Storage** | We utilize **Supabase** (EU/US cloud infrastructure) to store anonymous leaderboard scores and device session metadata. |
| **Device Hardware / Sensors** | Motion sensors (gyroscope/accelerometer) are read in real time for tilt steering. This data **never** leaves your device. |
| **Children's Privacy** | Fluffy Drift is designed to be family-friendly and complies with **COPPA** and **Google Play Families Policy**. We never knowingly collect personal data from children under 13 (or under 16 in applicable jurisdictions). |
| **Data Sale** | We **never** sell, rent, or trade your personal data for monetary consideration. |
| **Contact Email** | For any inquiries, rights requests, or feedback: **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)** |

---

## 3. Information We Collect and Process

### A. Information You Provide Directly
* **Player Display Name / Alias:** When you start Fluffy Drift, the game generates a friendly random pseudonym (e.g., `Drifter #4521`). You may freely edit or change this alias in the in-game settings. We strongly recommend that you **do not use your real name** or any personal information as your player handle.
* **Direct Communications & Feedback:** If you reach out to our support team via email at [allgames9e@gmail.com](mailto:allgames9e@gmail.com), we receive your email address, your message content, and any attachments or diagnostics you voluntarily submit. We use this information solely to answer your questions and provide technical assistance.

### B. Information Collected Automatically
When you run Fluffy Drift, the game and its underlying engine (Next.js, Three.js, Capacitor) automatically collect certain pseudonymous technical information:
1. **Pseudonymous Device Identifier:** A locally generated random token (stored under `fluffy_device_id`) used to recognize your device across game sessions, synchronize high scores, and prevent fraud.
2. **Device Specifications & Hardware Model:** Generic device model (e.g., Samsung Galaxy S23, Google Pixel, Android generic device), operating system type and version (e.g., Android 14), and screen resolution.
3. **Gameplay Telemetry & Statistics:** High score (distance traveled in meters), collected musical notes/stars, coin counters, active car skin/variant (`cloud`, `berry`, `mint`, `honey`), session count, playtime duration, and timestamp of last activity.
4. **Network & Connection Status:** IP address (processed temporarily by server hosts for network routing, DDoS prevention, and general country-level geographic routing; not stored alongside your identity).

### C. Sensor Data & Hardware Features
* **Accelerometer / Gyroscope (Motion Sensors):** Fluffy Drift supports optional motion/tilt steering. When enabled, your device's orientation sensor is accessed locally in real time to calculate car steering angles. **Sensor readings are processed purely in client-side RAM and are never recorded, logged, or transmitted over any network.**
* **Audio Hardware (Speakers / Headphones):** The game generates real-time procedural synthesizer audio and sound effects using the Web Audio API. **The game does NOT request or use microphone permissions and NEVER records audio.**

### D. Information We NEVER Collect
To provide full transparency, Fluffy Drift does **NOT** collect, request, or access:
- Real legal names, physical mailing addresses, or phone numbers;
- Financial details, credit card numbers, or bank accounts (all in-game items, fuel, and skins are unlocked purely through gameplay or watching rewarded ads);
- Contacts, address books, call logs, SMS, or file storage outside the game's sandbox;
- Camera or microphone inputs;
- Precise GPS or real-time location data;
- Biometric identifiers (fingerprints, facial geometry).

---

## 4. Local Storage and On-Device Data

Fluffy Drift uses on-device client storage (`localStorage` and internal app cache) to deliver a seamless, offline-tolerant experience. The specific storage items include:

| Storage Key | Data Stored | Purpose & Scope |
| :--- | :--- | :--- |
| `fluffy-drift-best-distance` | Numerical integer (e.g., `2450`) | Stores your personal high score locally on your device. |
| `fluffy-drift-car-variant` | String (`cloud`, `berry`, `mint`, `honey`) | Remembers your selected fluffy vehicle customization. |
| `fluffy_gyro_enabled` | Boolean (`true` / `false`) | Saves your steering preference (touch buttons vs. tilt steering). |
| `fluffy_device_id` | Pseudonymous random string | Anonymous device identifier for cloud high-score sync. |
| `fluffy_player_name` | String (e.g., `Drifter #7721`) | Your public leaderboard alias. |
| `fluffy_session_count` | Numerical counter | Measures total sessions played for game milestone tracking. |
| `fluffy_cached_ads_config` | JSON object | Caches ad network configuration for 0ms startup without lag. |
| `fluffy_policies_config_cache` | JSON object | Caches policy links, how-to-play guidelines, and support settings. |

*You can clear all locally stored data at any time by clearing Fluffy Drift's storage and cache in your Android device's **Settings > Apps > Fluffy Drift > Storage > Clear Data**.*

---

## 5. Third-Party Services and Software Development Kits (SDKs)

Fluffy Drift integrates trusted third-party SDKs to provide online leaderboards, remote updates, and ad-supported gameplay. Each provider processes data according to their respective privacy policies:

### 1. Google AdMob (Google LLC / Google Ireland Ltd.)
We serve advertisements to keep Fluffy Drift free for all players. We use the official Google AdMob SDK (via `@capacitor-community/admob`).

* **Ad Formats Utilized:**
  - **Banner Ads:** Docked non-intrusive banners at the bottom or top of the screen;
  - **Interstitial Ads:** Full-screen static or video ads shown occasionally between game-over rounds;
  - **Rewarded Ads:** Optional user-initiated ads that reward you with extra fuel or a revive upon completion;
  - **App Open Ads:** Ads displayed when launching or returning to the game from the background.
* **Data Processed by Google AdMob:**
  - Google Advertising ID (GAID / AAID);
  - Coarse geographic location derived from IP address (city/country level);
  - Diagnostic logs, ad impression measurements, click-through rates, and interaction timestamps;
  - Device characteristics (make, model, OS, language, carrier).
* **Ad Personalization & Opt-Out:**
  Depending on your region and preferences, ads may be personalized or non-personalized. You can opt out of personalized advertising at any time via your device settings:
  - **On Android:** Go to **Settings > Google > Ads > Delete Advertising ID** (or **Opt out of Ads Personalization** on older versions).
  - **Google Ad Settings:** Visit [https://adssettings.google.com](https://adssettings.google.com).
* **AdMob Privacy Policy:**  
  [https://policies.google.com/technologies/ads](https://policies.google.com/technologies/ads)  
  [https://policies.google.com/privacy](https://policies.google.com/privacy)

### 2. Supabase Cloud (Supabase, Inc.)
We use Supabase as our secure database and cloud infrastructure backend.

* **Purpose:**
  - Maintaining global high-score leaderboards (`app_leaderboard` table);
  - Recording anonymous device session counters and game version compatibility (`app_users` table);
  - Fetching remote configuration for maintenance announcements, app updates, and ad frequency.
* **Data Transmitted:**
  - Pseudonymous `device_id`, player alias, score, collected notes, app version, and timestamp of activity.
* **Security & Storage Location:**
  - Data is transmitted exclusively over encrypted HTTPS/TLS 1.3 channels.
  - Access is governed by Supabase Row-Level Security (RLS) policies.
* **Supabase Privacy Policy:**  
  [https://supabase.com/privacy](https://supabase.com/privacy)

### 3. Google Gemini API / AI Studio (Google LLC)
Fluffy Drift's architecture supports AI-assisted procedural content generation. Where invoked:
* Only contextual gameplay parameters (such as theme color tokens, track curvature parameters, or aesthetic prompts) are processed.
* **No personal data, user credentials, or player profiles are ever sent to the Gemini API.**
* **Google Privacy Policy:**  
  [https://policies.google.com/privacy](https://policies.google.com/privacy)

---

## 6. How We Use the Information We Collect

We use the collected information strictly for legitimate operational purposes:

1. **Core Gameplay & State Persistence:**
   - Saving your best drift distances, unlocked car skins, and audio preferences;
   - Calculating and rendering dynamic procedural tracks and horizon colors.
2. **Global Leaderboards & Fair Play:**
   - Displaying top scores on the world leaderboard;
   - Detecting and mitigating unnatural automated scoring or malicious activity.
3. **Advertising & Monetization:**
   - Serving relevant ads through Google AdMob to fund game development and server maintenance;
   - Providing in-game rewards (e.g., fuel revives) upon completing rewarded video ads.
4. **Maintenance, Quality & Diagnostics:**
   - Detecting runtime crashes, rendering freezes, or network disconnections;
   - Checking whether your installed version requires a critical maintenance update.
5. **Customer Support:**
   - Responding to feedback or technical bug reports submitted to [allgames9e@gmail.com](mailto:allgames9e@gmail.com).

---

## 7. Legal Bases for Processing (GDPR / UK GDPR)

If you are a resident of the European Economic Area (EEA), United Kingdom, or Switzerland, our processing of your information is justified under the following legal bases of the General Data Protection Regulation (Regulation (EU) 2016/679):

* **Legitimate Interests (Art. 6(1)(f) GDPR):** Processing pseudonymous device IDs, gameplay stats, and crash telemetry is necessary for our legitimate interests in operating, securing, debugging, and improving Fluffy Drift, provided your fundamental rights do not override these interests.
* **Consent (Art. 6(1)(a) GDPR):** Where required by applicable law (such as for personalized advertising or non-essential cookies/tracking IDs served by Google AdMob), we rely on your explicit consent obtained via the Google User Messaging Platform (UMP) or equivalent consent management tool. You may revoke consent at any time.
* **Performance of a Contract (Art. 6(1)(b) GDPR):** Providing basic game services, scores, and syncing your progress across game launches.
* **Legal Obligation (Art. 6(1)(c) GDPR):** When necessary to comply with binding legal requests, accounting rules, or regulatory mandates.

---

## 8. Children’s Privacy and Families Policy Compliance

Fluffy Drift is an engaging, family-friendly game featuring stylized pastel cars, soothing music, and non-violent driving mechanics. We place the highest priority on protecting children's privacy:

### Compliance with COPPA and Google Play Families Policy:
* **No Underage Data Harvesting:** We do **not** knowingly solicit, collect, or store personal information from children under the age of 13 (or under 16 in the EEA/UK), in strict compliance with the **Children’s Online Privacy Protection Act (COPPA)** and GDPR-K.
* **No Behavioral Retargeting:** In instances where Fluffy Drift is categorized under child-directed experiences or where a player indicates they are a child, advertising SDKs are configured to deliver only contextual (non-personalized) ads that comply with Google Play's Families Self-Certified Ads SDK requirements.
* **Parental Rights & Inquiries:** If you are a parent or legal guardian and believe that your child has provided us with any personal information, or if you wish to review, modify, or delete any data associated with your child's device, please contact us immediately at **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)**. Upon verification, we will promptly delete all such data from our systems.

---

## 9. California Consumer Privacy Rights (CCPA / CPRA)

If you are a California resident, the California Consumer Privacy Act (as amended by the California Privacy Rights Act) affords you specific rights regarding your personal information:

1. **Right to Know / Access:** You have the right to request details on the categories and specific pieces of personal information we have collected about you, the categories of sources, the business purposes for collecting it, and the categories of third parties with whom it was shared over the past 12 months.
2. **Right to Delete:** You have the right to request that we delete personal information collected from you, subject to certain legal exceptions.
3. **Right to Correct:** You have the right to request correction of inaccurate personal information.
4. **Right to Opt-Out of Sale or Sharing:** We **do not sell** your personal information for monetary payment. However, the sharing of pseudonymous advertising IDs with ad networks (like Google AdMob) for cross-context behavioral advertising may be considered "sharing" under California law. You can opt out by resetting or disabling your Android Advertising ID or contacting us.
5. **Right to Non-Discrimination:** We will never discriminate against you, deny you access to the game, charge different prices, or provide a lower quality of gameplay because you exercised any of your CCPA/CPRA rights.

To submit a request under the CCPA/CPRA, please contact us at **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)** with the subject line *"CCPA Privacy Request"*.

---

## 10. Your Rights Under GDPR (EEA & UK Users)

If you reside in the EEA or UK, you enjoy the following statutory rights under the GDPR:
* **Right of Access (Art. 15 GDPR):** Request a copy of the pseudonymous telemetry linked to your device ID.
* **Right to Rectification (Art. 16 GDPR):** Request correction of inaccurate information.
* **Right to Erasure / "Right to be Forgotten" (Art. 17 GDPR):** Request that your leaderboard entry and device telemetry be permanently purged.
* **Right to Restriction of Processing (Art. 18 GDPR):** Request that we restrict data processing under specific conditions.
* **Right to Data Portability (Art. 20 GDPR):** Receive your data in a structured, commonly used, and machine-readable format.
* **Right to Object (Art. 21 GDPR):** Object to data processing based on legitimate interests.
* **Right to Lodge a Complaint:** You have the right to lodge a complaint with your local data protection supervisory authority (e.g., the CNIL in France, the BfDI in Germany, or the ICO in the UK).

To exercise any of these rights, email us at **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)**. Because we do not store your name or email in our database, please provide your **Device ID** (found in game settings or retrieved via the storage key `fluffy_device_id`) so we can locate your record.

---

## 11. Android System Permissions Explained

Fluffy Drift requests only the minimal operating system permissions required for its functionality:

| Android Permission | Technical Rationale | Critical / Optional |
| :--- | :--- | :--- |
| `android.permission.INTERNET` | Required to communicate with Supabase for leaderboard scores, fetch remote settings, and load Google AdMob advertisements. | Required for online features |
| `android.permission.ACCESS_NETWORK_STATE` | Used by Capacitor and AdMob to detect whether an active Wi-Fi or cellular network is available before making requests. | Required for network resilience |

*Fluffy Drift does **NOT** request access to camera, microphone, GPS fine/coarse location, external storage, phone state, contacts, or Bluetooth.*

---

## 12. Data Retention and Security

### Data Retention
* **Leaderboard & Gameplay Scores:** Stored in our Supabase database for as long as the game remains active, or until you request deletion.
* **Device Telemetry Logs:** Pseudonymous active timestamps and session counters are retained for analytical maintenance and automatically purged or aggregated after 12 months of device inactivity.
* **Local Device Storage:** Persists on your physical phone until you uninstall the app or clear app data via device settings.
* **Support Inquiries:** Emails sent to [allgames9e@gmail.com](mailto:allgames9e@gmail.com) are retained for up to 180 days to resolve ongoing issues, after which they are securely archived or deleted.

### Data Security Measures
We implement comprehensive administrative, technical, and physical safeguards:
- **Encrypted Transmission:** All data exchanged between Fluffy Drift, Supabase, and Google AdMob is transmitted using Transport Layer Security (TLS 1.2 / TLS 1.3).
- **Pseudonymization by Design:** We do not link device IDs with real-world identities, phone numbers, or residential addresses.
- **Access Restrictions:** Cloud database credentials and production keys are strictly limited to authorized engineering personnel using role-based access control.

*Please note that no method of electronic transmission over the internet or method of digital storage is 100% impenetrable; while we strive to use commercially acceptable means to protect your information, absolute security cannot be guaranteed.*

---

## 13. International Data Transfers

Our service providers (including Supabase, Google LLC, and cloud content distribution networks) operate servers globally, including in the United States, the European Union, and other jurisdictions. By using Fluffy Drift, you understand that your pseudonymous technical data may be transferred to, stored, and processed in countries outside your country of residence, where data protection laws may differ.

Where personal data originates in the EEA or UK and is transferred internationally, our partners rely on approved transfer mechanisms, including the **European Commission’s Standard Contractual Clauses (SCCs)** or adequacy decisions (such as the EU-U.S. Data Privacy Framework).

---

## 14. Changes and Updates to This Privacy Policy

We may update this Privacy Policy from time to time to reflect modifications in our game features, third-party SDK updates, legal obligations, or operational practices. 

When changes are made:
- We will update the **"Last Updated"** date at the top of this document;
- For material changes that significantly affect your rights, we will provide a prominent notice within Fluffy Drift (such as an in-game alert or banner notification);
- The current version of this policy will always remain accessible inside the game's Settings menu (**Settings > Privacy Policy**) and publicly at our official repository URL:  
  `https://raw.githubusercontent.com/XyloGamix/FluffyDrift-legal-files/refs/heads/main/privacy-policy.md`.

We encourage you to review this Privacy Policy periodically to stay informed about how we are protecting your data.

---

## 15. How to Request Data Deletion

You have the right to request the permanent deletion of any data associated with your gameplay (including your leaderboard records and telemetry).

To request deletion:
1. Open Fluffy Drift on your device;
2. If you know your in-game nickname or generated Device ID (found in settings), note it down;
3. Send an email to **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)** with:
   - **Subject Line:** *Data Deletion Request - Fluffy Drift*
   - **Body:** Mention your player display name (e.g., `Drifter #1234`) and your approximate high score or Device ID.
4. We will verify and permanently delete your record from our Supabase tables within **30 days**, confirming the completion of your request via email.

---

## 16. Contact Information

If you have any questions, comments, concerns, complaints, or legal inquiries regarding this Privacy Policy or our data handling practices, please contact our Data Protection Officer / Development Team:

* **Developer / Publisher:** PlaySphere
* **Game Title:** Fluffy Drift (`com.playsphere.fluffydrift`)
* **Dedicated Privacy & Support Email:** **[allgames9e@gmail.com](mailto:allgames9e@gmail.com)**
* **Response Time:** We strive to acknowledge and address all inquiries within **48 to 72 business hours**.

---

*Copyright © 2026 PlaySphere. All rights reserved.*
