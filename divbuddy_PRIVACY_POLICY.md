# Privacy Policy for DivBuddy

**Effective Date:** September 29, 2026  
**Last Updated:** September 29, 2026

DivBuddy ("we", "our", or "us") provides a group expense splitting and debt settlement mobile application (the "App", package name: `com.rdba.divbuddy`). We are committed to protecting your privacy and being transparent about how data is handled.

Please read this Privacy Policy carefully to understand our practices regarding your information.

---

## 1. Overview & Privacy-First Architecture

DivBuddy is designed with privacy and local-first principles in mind:
- **No Account Required:** You can use DivBuddy entirely offline without creating an account or signing in. All expense calculations and group ledgers remain securely on your device.
- **Optional Cloud Sync:** Cloud synchronization and group collaboration features are optional and only enabled when you choose to sign in with Google and create or join shared groups.
- **On-Device Receipt Processing:** Receipt scanning uses optical character recognition (OCR) that runs 100% on your device. Receipt images are never uploaded to any cloud server.

---

## 2. Information We Collect and How We Use It

### A. Information You Provide Directly
* **User Profile (Optional):** If you choose to sign in with your Google account via Firebase Authentication, we collect your name, email address, and profile picture URL. This is used solely to authenticate you and display your identity to fellow members in shared groups.
* **Expense and Group Data:** Information you input to track expenses, such as group names, member names, expense descriptions, amounts, dates, split distributions, and settlement records.
  * For local groups, this data is stored exclusively in your device's local database (SQLite).
  * For shared groups, this data is synchronized via Google Cloud Firestore so that authorized members of the group can view and edit the ledger.
* **Pro Waitlist (Optional):** If you voluntarily sign up for early access to upcoming Pro features, we collect your email address via Web3Forms solely to notify you about Pro availability.

### B. Device Permissions and On-Device Data
* **Camera & Photo Library (`CAMERA`, `READ_EXTERNAL_STORAGE` / Media Access):**
  * **Purpose:** To photograph or select receipt images for expense itemization.
  * **On-Device Processing:** DivBuddy processes images using Google ML Kit on-device text recognition.
  * **Zero Cloud Storage:** **Receipt photos are never uploaded to, transmitted to, or stored on any remote servers.** All processing occurs in local device memory.
* **Device Contacts (`READ_CONTACTS` - Optional):**
  * **Purpose:** Used strictly within the contact picker to help you easily select names or email addresses when adding members to an expense group.
  * **No Harvesting:** DivBuddy **never** uploads, stores, scrapes, or syncs your contact list or address book to any external server. Only the specific contact you manually select is placed into the group member form.
* **Notifications (`POST_NOTIFICATIONS`):**
  * **Purpose:** Used to send push notifications regarding group invitations and expense updates for groups you participate in.

### C. Automatically Collected Information & Advertising
* **Google AdMob (`react-native-google-mobile-ads`):**
  * DivBuddy includes rewarded video advertisements that allow users to earn in-app virtual coins.
  * AdMob (provided by Google LLC) may collect device identifiers (such as Google Advertising ID / GAID), IP address, app performance data, and diagnostics to serve rewarded ads, prevent fraud, and measure ad performance.
  * For details on how Google uses information from sites or apps that use its services, visit [Google's Advertising Privacy Policies](https://policies.google.com/technologies/ads).
* **Virtual Economy (Coins):**
  * DivBuddy uses a local virtual currency ("coins") to manage expense additions and split exports. Coin balances and claim timers are stored locally on your device and are never linked to real money or sold.

---

## 3. Third-Party Services

We integrate with trusted third-party service providers that process data under strict data protection terms:

1. **Google Firebase (Google LLC):**
   * **Firebase Authentication:** Secure sign-in management.
   * **Cloud Firestore:** Encrypted cloud storage for shared group data.
   * **Firebase Cloud Messaging (FCM):** Push notification delivery.
   * [Google Privacy Policy](https://policies.google.com/privacy) | [Firebase Data Privacy and Security](https://firebase.google.com/support/privacy)
2. **Google AdMob (Google LLC):**
   * Rewarded advertising network.
   * [Google AdMob Policies & Privacy](https://support.google.com/admob/answer/6128543)
3. **Web3Forms:**
   * Used solely for processing optional Pro waitlist email submissions.
   * [Web3Forms Privacy Policy](https://web3forms.com/privacy)

---

## 4. Data Sharing and Disclosure

We do not sell, rent, trade, or monetize your personal information. Your information is shared only in the following contexts:
* **With Group Members:** In shared groups, your name, email, and the expenses or settlements you record are visible to other members explicitly invited to that specific group.
* **Legal Requirements:** We may disclose your information if required to do so by applicable law, regulation, legal process, or governmental request.

---

## 5. Data Retention, Storage, and Security

* **Security:** All data transmitted between the App and Firebase servers is encrypted in transit using industry-standard Transport Layer Security (HTTPS/TLS). Cloud Firestore database rules enforce authentication checks for group access.
* **Local Data Retention:** Data stored locally on your device remains until you clear the application data, use the "Reset App" button in Settings, or uninstall the App.
* **Cloud Data Retention:** Data in shared groups persists as long as the group exists. When a group owner deletes a shared group, it is permanently deleted from the cloud database.

---

## 6. Your Rights and Data Deletion

You have the following rights regarding your data:
* **Access & Portability:** You can view all your expenses and members directly within the App, and export group summaries via the in-app export feature.
* **Deletion of Local Data:** You can delete all local data at any time by going to **Settings > Reset all data** or clearing the application data through Android device settings.
* **Deletion of Cloud Data / Account:**
  * **In-App Account Deletion:** You can delete your Firebase account and cloud profile directly in the App at **Settings > Account identity > Delete account**.
  * **Web Request Form:** If you have uninstalled the App, you can submit an account and data deletion request via our [Account Deletion & Data Request Page](delete-account.html).
  * **Email Request:** You may also email **support@yourdomain.com** with the subject line *"Data Deletion Request"*. All valid requests are processed within 30 days.

---

## 7. Children's Privacy

DivBuddy is a general-audience financial utility tool and is not directed at or intended for children under the age of 13 (or under 16 in the European Economic Area). We do not knowingly collect personal information from children. If you believe that a child has provided us with personal information, please contact us immediately so we can remove it.

---

## 8. Changes to This Privacy Policy

We may update this Privacy Policy from time to time. Any changes will be posted on this page with an updated "Last Updated" date. We encourage you to review this policy periodically.

---

## 9. Contact Us

If you have questions, feedback, or data requests regarding this Privacy Policy, please contact us at:

- **Developer / Company:** DivBuddy Team
- **Email:** [support@yourdomain.com] *(Replace with your contact email)*
- **Website:** [https://yourdomain.com] *(Optional)*
