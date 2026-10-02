# Google Play Store Submission & Policy Compliance Guide

A complete, step-by-step checklist to review and submit **MindBuddy** (`com.rdba.mindbuddy`) on the **Google Play Console**, ensuring full compliance with Google's latest policies (Health, Data Safety, Sensitive Events, Advertising, Permissions).

---

## Quick Reference Summary

| Field | Configuration / Value |
| :--- | :--- |
| **App Name** | `MindBuddy: Focus & Breathwork` (29 chars) |
| **Package ID** | `com.rdba.mindbuddy` |
| **Primary Category** | Productivity |
| **Secondary Category** | Health & Fitness / Mindfulness |
| **Developer Contact Email** | `mybuddyappsupport@gmail.com` |
| **Privacy Policy URL** | Host `docs/PRIVACY_POLICY.md` (e.g. GitHub Pages or raw public URL) |
| **Target Audience** | 13+ (Ages 13 and older) |
| **Ads Present?** | **Yes** (Google AdMob banner & rewarded ads) |
| **Contains Health Features?** | Yes (General Mindfulness & Breathing; **NOT a medical device**) |

---

## 1. App Content & Policy Questionnaire Checklist

In Google Play Console, go to **Policy and programs** > **App content**. You must complete every section below:

### A. Privacy Policy
- **Requirement:** Must be a valid, public, HTTPS link.
- **Action:** Upload/render [docs/PRIVACY_POLICY.md](file:///c:/Work/Projectos/testesai/MindBuddy/docs/PRIVACY_POLICY.md) to a public site (e.g., GitHub repository markdown viewer or GitHub Pages) and paste the URL here.
- **Verify:** Ensure contact email shows `mybuddyappsupport@gmail.com`.

### B. Health Apps Policy (Crucial for Review Approval)
- **Question:** Does your app provide health, wellness, or medical-related features?
  - **Answer:** **Yes**
- **Question:** Select the categories that apply to your app:
  - **Answer:** Select **"Health management and well-being"** or **"Relaxation / Mental wellbeing"**.
  - **DO NOT select:** Medical Device, Disease Management, Telehealth, or Clinical Care.
- **Question:** Is the app a medical device or certified software under FDA/CE?
  - **Answer:** **No**.
- **Declaration Note:** The description and privacy policy both state: *"MindBuddy is strictly a mindfulness and productivity companion for general relaxation and focus tracking. It is not a medical device and provides no medical diagnosis or treatment."*

### C. Data Safety Questionnaire
When answering the Data Safety questions:

1. **Does your app collect or share any of the required user data types?**
   - **Answer:** **Yes** (Due to the Google Mobile Ads / AdMob SDK).
2. **Is all user data collected by your app encrypted in transit?**
   - **Answer:** **Yes** (All network communications by Google AdMob use HTTPS).
3. **Do you provide a way for users to request that their data be deleted?**
   - **Answer:** **Yes** (Users can clear local app data or email support to remove waitlist emails).
4. **Data Types Breakdown to Declare:**
   - **Device or other IDs** (`Device or other IDs`):
     - *Collected:* Yes (by AdMob SDK).
     - *Shared:* Yes (with Google for advertising & analytics).
     - *Purposes:* **Advertising or marketing**, **Analytics**, **Fraud prevention, security, and compliance**.
     - *Ephemeral:* No.
     - *Is this data required or optional?*: Required by the ad provider.
   - **Personal Info (Email address)**:
     - *Collected:* Optional (only if the user voluntarily submits their email for the Pro Waitlist).
     - *Shared:* No (never shared or sold to third parties).
     - *Purposes:* App functionality / Account communication (waitlist notifications).
   - **Health and Fitness Data**:
     - *Collected or Shared:* **No** (All Pomodoro timers and breathing counts are kept 100% locally on the device in `AsyncStorage` and never uploaded to any server).

### D. Ads (Advertising Declaration)
- **Does your app contain ads?**
  - **Answer:** **Yes**.
- **Advertising ID (AAID):**
  - Does your app use Advertising ID?
  - **Answer:** **Yes**. Under *Why does your app use advertising ID?*, check **Advertising or marketing** and **Analytics** (via Google Mobile Ads SDK).

### E. Target Audience and Content (COPPA & Families)
- **Target Age Groups:**
  - Check **13-15**, **16-17**, and **18 and over**.
  - **DO NOT check under 13** unless you plan to comply with Google Play's strict Families Policy and Designed for Families ad network rules.
- **Could your store listing appeal to children?**
  - **Answer:** **No** (The aesthetic is productivity/minimalist meditation, not children's cartoons).

### F. Financial Features / In-App Coins Declaration
- **Does your app provide financial features or real-money gaming?**
  - **Answer:** **No**.
- Note: Coins in MindBuddy are strictly virtual progression utilities with zero monetary value and cannot be exchanged for cash or cryptocurrencies.

### G. Government Apps
- **Is your app developed by or on behalf of a government entity?**
  - **Answer:** **No**.

### H. News Apps
- **Is your app a news app?**
  - **Answer:** **No**.

### I. Content Rating (IARC Questionnaire)
In Play Console, go to **Policy and programs** > **App content** > **Content ratings** > **Start questionnaire**:
1. **Email address:** `mybuddyappsupport@gmail.com`
2. **Category:** Select **Utility, Productivity, Communication, or Other**. *(Do NOT select Game or Social Networking).*
3. **Questionnaire Answers:**
   - **Violence:** No (Does not contain violent materials or depictions).
   - **Sexuality:** No (No sexual content or nudity).
   - **Language:** No (No profanity or crude language).
   - **Controlled Substances:** No (No references to drugs, alcohol, or tobacco).
   - **Promotion of age-restricted goods:** No.
   - **Miscellaneous:**
     - *Does the app natively allow users to interact or exchange content with other users through voice, text, or sharing images?* **No** (Local-only app, no chat or user posts).
     - *Does the app share the user's current and precise physical location?* **No**.
     - *Does the app allow users to purchase digital goods?* **No** (Coins are earned free via timers, bonuses, or rewarded ads; no in-app purchases).
     - *Does the app contain any offensive or sensitive political symbols?* **No**.
4. **Summary / Result:** 
   - Yields **PEGI 3**, **ESRB Everyone**, **USK 0**, and universal **Everyone** ratings across all global territories.
   - Click **Save** then **Submit**.

---

## 2. Permissions Declarations

Google reviews Android permissions closely. Below is the justification for every permission in `app.json`:

| Permission | Review Rationale / Declaration |
| :--- | :--- |
| `POST_NOTIFICATIONS` | Used to alert users when a focus block or break period ends so they know when to take a break or resume work. |
| `SCHEDULE_EXACT_ALARM` | Required for reliable Pomodoro timer countdowns and accurate phase completion alarms when the device is locked/sleeping. |
| `RECEIVE_BOOT_COMPLETED` | Reschedules active reminders and daily streak trackers if the device is rebooted. |
| `FOREGROUND_SERVICE` | Base Android foreground service permission required to maintain background service tasks. |
| `FOREGROUND_SERVICE_MEDIA_PLAYBACK` | Allows uninterrupted ambient focus soundscapes (Rain, Brown Noise, Zen Bells) to play in the background while users work in other apps or lock their screens. |
| `MODIFY_AUDIO_SETTINGS` | Controls volume levels and audio ducking/crossfading between sound loops and completion bells. |

### Foreground Service (FGS) Media Playback Declaration Form
Google Play Console enforces a dedicated policy declaration under **Policy and programs** > **App content** > **Foreground service permissions** for `FOREGROUND_SERVICE_MEDIA_PLAYBACK` on Android 14+ (API level 34+). Complete it as follows:

1. **Service Type Selection:**
   - Select: **Media playback** (`FOREGROUND_SERVICE_MEDIA_PLAYBACK`).
2. **Video Demonstration Link:**
   - Provide a publicly accessible link (e.g., YouTube unlisted, Google Drive with "Anyone with link can view") demonstrating the feature in action:
     - Open MindBuddy.
     - Start an ambient soundscape (e.g. Rain or Brown Noise) or a focus session.
     - Leave the app (go to the home screen or lock the phone / turn off the screen).
     - Show that the soundscape continues playing seamlessly in the background and can be paused/controlled via notification or returning to the app.
3. **Core Functionality Justification (Copy-Paste Text):**
   > *"MindBuddy is a Pomodoro productivity and breathwork app designed for deep, sustained focus. Users listen to uninterrupted ambient audio soundscapes (such as rain, brown noise, ocean swells, and singing bowls) during multi-minute focus intervals. The foreground media playback service allows these ambient sounds to continue playing continuously when the user locks their screen or switches between other work apps (documents, IDEs, spreadsheets) without the operating system prematurely terminating the audio process."*
4. **User-Initiated Trigger:**
   - Indicate that audio playback is explicitly initiated by the user when they choose a soundscape preset or start a focus timer.

---

## 3. Store Presence & Graphic Assets Checklist

Under **Grow** > **Store presence** > **Main store listing**:

- [ ] **App Title:** `MindBuddy: Focus & Breathwork`
- [ ] **Short Description:** `Pomodoro focus timer with guided breathwork, zen bells & ambient soundscapes.`
- [ ] **Full Description:** Copy text from [PLAY_STORE_RELEASE.md](file:///c:/Work/Projectos/testesai/MindBuddy/PLAY_STORE_RELEASE.md).
- [ ] **App Icon:** 512 x 512 PNG (32-bit color, no transparency). Located at `./assets/images/icon-foreground-512.png` or generated via `node scripts/generate-icons.js`.
- [ ] **Feature Graphic:** 1024 x 500 JPG or PNG.
- [ ] **Phone Screenshots:** At least 4 screenshots (1080 x 1920 or 1080 x 2400) showing:
  1. Focus timer in action with amber overtime ring.
  2. Guided breathwork modal (Box / 4-7-8 breathing circle).
  3. Ambient audio player drawer (Rain, Stream, Singing bowl).
  4. Consistency streak & 14-day history sequence.

---

## 4. Pre-Release Build & Version Check

Before uploading your `.aab` file:

1. **Verify Version Drift:**
   ```bash
   node scripts/show-version.js --variant aab
   ```
   *Make sure `app.json` and `build.gradle` match and the `versionCode` is higher than any previous upload.*

2. **Run TypeScript Check:**
   ```bash
   npx tsc --noEmit
   ```

3. **Verify AdMob Production IDs:**
   Ensure production AdMob ad unit IDs are configured in `app.json` (`extra.adMob.android`) and `USE_TEST_ADS = false` in `lib/adIds.ts`.

4. **Export / Bundle:**
   Build the release AAB using your release script or EAS:
   ```bash
   scripts\build-release-aab.bat
   ```
   *(Or EAS build if configured: `eas build --platform android --profile production`)*

---

## 5. Submitting for Review

1. Go to **Testing** > **Closed testing** (or **Production**).
2. Create a new release and upload the `.aab` from `android/app/build/outputs/bundle/release/app-release.aab`.
3. Enter Release Notes in English and supported languages (from [PLAY_STORE_RELEASE.md](file:///c:/Work/Projectos/testesai/MindBuddy/PLAY_STORE_RELEASE.md)).
4. Click **Review release**, verify no red blocking errors appear, then click **Start rollout to Production** (or Closed Testing).
