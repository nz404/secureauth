<div align="center">

# 🔐 SecureAuth — Privacy Policy

### *Your codes. Your phone. Nobody else's business.*

**Last updated:** November 19, 2026 · **App version:** 1.0.0 · **Developer:** Nz404

</div>

---

## 🧾 The 10-second version

| Question | Answer |
|---|---|
| Do you collect my data? | **No.** Not a single byte. |
| Do you have an account system? | **No.** Nothing to sign up for. |
| Do you use analytics, ads or crash-reporting services? | **No.** |
| Where are my 2FA secrets? | **Only on your phone**, encrypted. |
| Can the developer see my accounts or backups? | **No.** We have no server and no access. |
| Does the app use the internet? | **Only** if *you* turn on Google Drive backup. |

If that's all you wanted to know, you're done. 🎉 The rest explains it in detail.

---

## 🏠 1. Where your data lives

Everything you add to SecureAuth (account names, issuers, secret keys, folders, settings) is stored **only on your device**.

- 🗄️ Accounts are kept in an **encrypted database (SQLCipher)**.
- 🔑 The database key is protected by the **Android Keystore** and never leaves your phone.
- 🧮 All one-time codes are generated **locally**. No server is involved.
- 🙈 Optional **Screen security** blocks screenshots, screen recording and the recent-apps preview.
- 🔒 Optional **biometric / device PIN lock** protects the app.

> The developer runs **no servers** for this app, so there is nothing for us to receive, store or sell.

---

## 🚫 2. What we do NOT do

- ❌ No analytics, advertising, attribution or telemetry SDKs
- ❌ No Firebase, Crashlytics or similar services
- ❌ No selling, renting or sharing of personal data
- ❌ No user profiles, tracking or fingerprinting
- ❌ No Android Auto Backup or device-transfer of app data (turned off on purpose)

---

## 🔑 3. Permissions, explained

SecureAuth asks for as little as possible:

| Permission | Why | What happens to the data |
|---|---|---|
| 📷 **Camera** | Scan 2FA QR codes | Frames are processed in memory on your device and discarded. Never stored, never sent. |
| 🌐 **Internet** | Only for the optional Google Drive backup | Not used at all unless you connect Google Drive. |

**Not requested:** contacts, location, microphone, phone, SMS, or storage access.

🖼️ **Picking a QR image from your gallery** uses the Android photo picker. The app can read **only the image(s) you choose**, looks for a QR code in memory, and does not keep or upload the image.

---

## ☁️ 4. Google Drive backup (optional)

Off by default. If you turn it on:

1. You sign in with **Google**, handled by Google Play services under Google's own policies.
2. The app asks for one narrow permission: `drive.appdata`. That is a **hidden, private folder** that belongs to this app inside *your* Drive. The app **cannot see any other file** in your Drive.
3. Before anything leaves your phone, your backup is **encrypted on-device with AES-256-GCM**, using a key derived from **your backup password** (PBKDF2-HMAC-SHA256, 600,000 iterations).
4. The encrypted file goes **straight to your own Google Drive**. It does not pass through any server of ours.

What this means for you:

- 🕵️ The developer **cannot** read your backups.
- 🔐 **Forget your backup password and the backup cannot be recovered.** We can't reset it. Nobody can.
- 📱 To make automatic backups work in the background, the backup password is stored on your device, **wrapped by the Android Keystore**. The email of the Google account you connected is also kept on your device so the app can reconnect.
- ⏱️ Auto-backup runs in the background at the interval you choose (optionally Wi-Fi only) and skips the upload when nothing has changed.

### 🧹 Removing Drive access completely

The **Disconnect** button only clears the local session in the app. To fully remove access:

1. Open <https://myaccount.google.com/permissions>
2. Choose **SecureAuth** → **Remove access**
3. To delete the backup file: Google Drive → **Settings** → **Manage apps** → SecureAuth → **Delete hidden app data**

---

## 📁 5. Files you export or import

- **Export** creates an encrypted `.authbak` file at the location you choose.
- **Import** reads the file you pick (SecureAuth, 2FAS, Aegis, andOTP, Bitwarden, or a list of `otpauth://` links, plus Google Authenticator QR codes). Files are read on your device and are not uploaded anywhere.
- Plain-text exports from other apps are **unencrypted by nature**. Keep them safe and delete them after importing.

---

## 🧩 6. Home-screen widget

The optional widget shows codes **on your own home screen**. Codes stay hidden (`••••••`) until you tap to reveal them, and everything is calculated on your device. Anyone who can see your unlocked home screen can see a revealed code, so use it with that in mind.

---

## 🐞 7. Error logs

If the app stops unexpectedly, a short technical report is saved **only on your device**. It is **never sent anywhere**. You can copy it yourself if you want to report a problem.

---

## 🗑️ 8. Your control and deleting your data

- Delete any account or folder in the app at any time.
- **Uninstalling the app removes all local data.**
- Remove Drive access and the Drive backup using the steps in section 4.

Because the developer holds no data about you, there is nothing on our side to export or delete.

---

## 👶 9. Children

SecureAuth is a general-purpose security tool and is not directed at children. We do not knowingly collect data from anyone, including children.

---

## 🔗 10. Google API Services disclosure

SecureAuth's use and transfer of information received from Google APIs adheres to the [Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy), including the **Limited Use** requirements.

---

## 🔄 11. Changes to this policy

If the app changes in a way that affects privacy, this page will be updated and the date at the top will change. Because we collect no contact details, the date on this page is the way to see what's new.

---

## 💬 12. Contact

Questions, bug reports or privacy concerns?

📧 **nz404dev@gmail.com**
🐙 **GitHub:** open an issue in this repository

<div align="center">

---

*Made with ☕ by Nz404 — a 2FA authenticator that keeps your secrets where they belong: with you.*

</div>
