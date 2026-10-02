# Privacy Policy for MindBuddy

**Effective Date:** October 2, 2026  
**Last Updated:** October 2, 2026

MindBuddy ("we," "our," or "us"), developed by Ricardo Barbosa (`ricardodbarbosa`), provides a focused Pomodoro timer, guided breathing exercises, and ambient soundscapes mobile application (the "App", package `com.rdba.mindbuddy`).

We are committed to protecting your personal privacy and maintaining transparency regarding how your data is handled. This Privacy Policy details our data practices and addresses all requirements set forth by Google Play Developer Policies, including the **Health Apps Policy**, **User Data Policy**, **Children's Online Privacy Protection Act (COPPA)**, and **Advertising / AdMob Data Disclosures**.

---

## 1. Important Medical & Health Disclaimer (Google Play Health Apps Policy)

> **MindBuddy is NOT a Medical Device.**  
> MindBuddy is designed strictly for general mindfulness, productivity, focus time tracking, and everyday stress reduction / relaxation.

- **No Medical Advice:** The breathing exercises (such as Box Breathing, 4-7-8, Energizing), audio tones, and timer pacing in the App are intended for wellness and lifestyle enhancement only. They are not intended for use in the diagnosis, cure, mitigation, treatment, or prevention of any medical condition, disease, anxiety disorder, sleep apnea, or physiological ailment.
- **Consultation:** Always seek the advice of your physician or qualified healthcare provider with any medical questions or before starting any new breathing regimen if you have pre-existing cardiovascular, respiratory, or neurological conditions. Never disregard professional medical advice or delay seeking it because of something you have experienced or read within this App.
- **No Health Connect / Protected Health Records:** MindBuddy does **not** integrate with or write to Google Health Connect, Apple HealthKit, or electronic health record (EHR) systems. We do not access, process, transmit, or store any Protected Health Information (PHI) or biometric measurements (e.g., heart rate, blood pressure, SpO2).

---

## 2. Information We Collect and How We Use It

MindBuddy is designed with a **privacy-first, local-first architecture**. 

### A. Information Stored Locally on Your Device
The following data is created and saved **exclusively on your device** using local storage (`AsyncStorage`):
- **Focus & Session History:** Timestamps of your focus, short break, and long break sessions, actual elapsed minutes, completion status, and cycle counts.
- **Breathing & Streak Progress:** Completed breathing cycles, active streaks, and day-by-day consistency markers.
- **Coins Balance & Rewards:** Virtual in-app coins earned via daily bonuses, hourly claims, or optional rewarded ads.
- **User Settings & Preferences:** Chosen ambient sounds, audio volume, timer lengths, breathing patterns, sound reminder toggles, language (EN, FR, ES, PT), and theme (Dark/Light).

*Note: This data never leaves your device unless you explicitly export a JSON backup using the manual Export feature.*

### B. Information Collected by Third-Party Services
We partner with select third-party service providers to deliver essential app features, such as monetization through non-intrusive advertisements:

#### Google AdMob (Google Play Services)
MindBuddy displays banner ads and optional user-initiated rewarded ads (for earning virtual coins) powered by Google AdMob (`react-native-google-mobile-ads`). 
Google AdMob may collect and process certain information in accordance with [Google's Privacy & Terms](https://policies.google.com/privacy) and Google Play's Families & Advertising Policies:
- **Device & Advertising Identifiers:** Google Advertising ID (AAID on Android), IP address, and general device specifications (e.g., model, OS version).
- **Diagnostics & Analytics:** Ad impressions, clicks, performance metrics, and crash/diagnostic logs for fraud prevention and network security.
- **Ad Personalization:** Depending on your device settings and consent, Google may serve personalized or non-personalized ads. You can reset or disable personalized ads at any time via your device settings (`Settings` > `Google` > `Ads`).

#### Pro Waitlist (Optional)
If you voluntarily choose to sign up for our MindBuddy Pro early-access waitlist, you may submit your email address. This email address is used solely for notifying you about future updates and discounts regarding MindBuddy Pro. We never sell, rent, or trade your email address to third parties.

---

## 3. Device Permissions & Rationale

MindBuddy requests only minimal permissions necessary to perform its advertised features:

| Permission | Android Identifier | Purpose & Rationale |
| :--- | :--- | :--- |
| **Notifications** | `POST_NOTIFICATIONS` | Sends local notifications to alert you when a focus session or break timer has ended. |
| **Exact Alarms** | `SCHEDULE_EXACT_ALARM` | Ensures precision timing for Pomodoro intervals and breathing transitions even when the screen is locked or the app is minimized. |
| **Boot Completed** | `RECEIVE_BOOT_COMPLETED` | Restores scheduled reminders and daily bonus resets if your device is restarted. |
| **Audio Settings** | `MODIFY_AUDIO_SETTINGS` | Adjusts playback volume and routing for ambient soundscapes and Tibetan singing bowl dings. |
| **Foreground Service (Media)** | `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Allows continuous playback of ambient focus sounds (rain, brown noise, cafe) in the background while you focus in other apps or lock your phone. |

MindBuddy **does NOT request or access**:
- Precise or approximate GPS location
- Camera or microphone
- Contacts or phone state
- Body sensors or physical activity permissions
- Storage/Filesystem access beyond user-initiated export/import file dialogs

---

## 4. Data Sharing and Disclosure

- **No Sale of Personal Data:** We do not sell, rent, or lease personal information or usage histories to third parties or data brokers.
- **Third-Party Service Providers:** We only share data with Google AdMob as described in Section 2(B) to support in-app advertising.
- **Legal Compliance:** We may disclose information if required by applicable law, regulation, legal process, or governmental request.

---

## 5. Data Retention, Backup, and Deletion Rights

- **Local Data Retention:** All session logs, settings, and streak metrics remain stored in your device's local application sandbox until you clear the app data or uninstall the App.
- **Exporting Your Data:** You can export all session records as a structured JSON file at any time via the History/Settings screen.
- **Data Deletion:** 
  - To delete all stored data, simply clear the App's storage via your device settings (`Settings` > `Apps` > `MindBuddy` > `Storage` > `Clear Storage/Data`) or uninstall the App.
  - If you submitted your email for the optional Pro Waitlist and wish to have it deleted from our records, you may email us at any time (contact details below), and we will delete your record within 30 days.

---

## 6. Children's Privacy (COPPA & Google Play Families Policy)

MindBuddy is intended for general audiences aged 13 and older (or the applicable age of digital consent in your jurisdiction). We do not knowingly target, market to, or collect personal information from children under the age of 13. If you believe that a child has provided us with personal information without parental consent, please contact us immediately so we can promptly remove such information.

---

## 7. Security

We take reasonable technical and administrative precautions to safeguard your information. Because user session data and streak analytics are retained locally on your own device rather than on external servers, the security of your timer logs is protected by your device's native operating system encryption and sandbox model.

---

## 8. International Users (GDPR & CCPA/CPRA)

If you are a resident of the European Economic Area (EEA), UK, or California:
- **Right to Access & Portability:** You have the right to access and export your data directly through the in-app JSON export function.
- **Right to Erasure:** You can erase all data directly by clearing app storage or contacting us for waitlist email removal.
- **Right to Object / Opt-Out:** You can opt out of personalized tracking via Google's ad personalization settings on your Android device.

---

## 9. Sensitive Events Policy (Google Play Policy Compliance)

Google Play strictly prohibits apps from capitalizing on or profiting from sensitive events, such as public health emergencies, natural disasters, conflicts, or tragic events.

- **No Exploitation of Sensitive Events:** MindBuddy is strictly a personal focus, mindfulness, and productivity utility. We do not claim to treat, mitigate, prevent, or diagnose illnesses or conditions related to global or regional health emergencies (e.g., pandemics, epidemics).
- **No Misleading Claims or Price Gouging:** MindBuddy does not exploit tragic events, civil emergencies, or natural disasters for commercial gain, promotional opportunism, or user acquisition.
- **Accurate Context:** The app does not display news alerts or broadcast emergency claims. Any mindfulness practices offered are general relaxation techniques and must never replace official emergency directives or medical advice during critical events.

---

## 10. Prevention of Deception, Misrepresentation, and Abuse

In strict compliance with Google Play's **Deceptive Behavior and Misrepresentation Policies**:

- **No Deceptive Functionality:** MindBuddy performs strictly as advertised. The timer, soundscapes, breathing exercises, and streak tracking function exactly as described in app listings and documentation without hidden behaviors, unauthorized background data harvesting, or spoofed interfaces.
- **Truth in Advertising & Rewards:** The in-app coin balance system operates with full transparency:
  - Coins earned through daily bonuses, hourly claims, or optional rewarded ads are clearly displayed.
  - Coins are virtual in-app utilities used solely to initiate timers and unlock local features (such as JSON exports); they have no real-world cash value and cannot be redeemed for fiat currency.
  - The App does not employ deceptive mechanics, forced clicks, misleading ad placements, or fake close buttons ("dark patterns").
- **No Impersonation or False Affiliation:** MindBuddy does not mimic, spoof, or misrepresent affiliation with any official health organization, governmental body, or medical institution.
- **Malware, Abuse & Security:** MindBuddy contains no spyware, trojans, adware, or unauthorized background payloads. The app adheres to secure coding standards and utilizes only official, audited libraries (such as Google Mobile Ads SDK and Expo modules).

---

## 11. Changes to this Privacy Policy

We may update this Privacy Policy from time to time to reflect changes in our practices, app features, or regulatory requirements. We will update the "Last Updated" date at the top of this policy and notify users via an app update or release notes.

---

## 12. Contact Us

If you have questions, feedback, or concerns regarding this Privacy Policy or our privacy practices, please contact us at:

- **Developer:** Ricardo Barbosa
- **App Name:** MindBuddy
- **Package ID:** `com.rdba.mindbuddy`
- **Email:** mybuddyappsupport@gmail.com *(or contact via GitHub repository: [ricardodbarbosa/MindBuddy](https://github.com/ricardodbarbosa/MindBuddy))*
