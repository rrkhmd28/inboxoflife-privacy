---
layout: default
title: InboxOfLife Privacy Policy
---

# InboxOfLife Privacy Policy

**Last updated**: 2026-05-28
**App**: InboxOfLife (iOS, distributed on the App Store)
**Languages**: [日本語](./) / English (this page)

---

## 1. Introduction

InboxOfLife ("the App") is a personal life-logging app developed and operated by Ruriko ("the Developer"). This Privacy Policy explains what information the App handles.

The App is **local-first**. Content the user enters (tasks, habits, calendar events, shopping items, wishlist items, memos, health notes, activity logs, chat history) is, as a rule, stored only in a local database on the user's device.

---

## 2. Developer

- Developer: Ruriko
- Contact: rrkhmd28@gmail.com

---

## 3. Information Collected

### 3.1 Stored on the user's device

The following is stored only in a local database on the user's device (SQLite via WatermelonDB). **Neither the Developer nor any third party can access this data directly** (except via the device's own cloud backup, if enabled by the user):

- Tasks, scheduled events, habits, shopping items, wishlist items, memos, health notes, and activity logs entered by the user
- Creation and update timestamps
- In-app chat history (previous inputs and their classification results)
- App preferences (notification settings, home-screen display priorities, etc.)

This data is removed from the device when the App is uninstalled.

### 3.2 Sent to the server (for AI classification)

To classify the user's free-form input into the right category, the following is sent to the Developer's server (hosted on Railway):

- The natural-language text the user typed
- A minimal context window to improve classification accuracy:
  - A few of the most recent chat turns
  - References (title, category, id) to recently saved entries
  - Titles of currently open habits, shopping items, tasks, and wishlist items (so the AI can recognize "completion" reports for existing items)

The server forwards the request to the third-party AI services described below (Google Gemini / OpenAI) and returns the result to the user's device. **The server does not persist the request body**.

### 3.3 Server-side logs

By default behavior of the hosting provider (Railway), the following access-log metadata is retained for a short period (around 30 days):

- IP address
- Request timestamp
- HTTP status code
- Endpoint path

These are used only for incident investigation and to detect abuse. They are not shared with third parties.

### 3.4 What we do NOT collect

The App does **not** collect:

- Account information (the App has no sign-in)
- Name, phone number, or address
- Contacts (address book)
- Location (GPS)
- Photos or camera data
- HealthKit / Apple Health data
- The advertising identifier (IDFA)
- In-app behavioral analytics or tracking
- Crash reports (not enabled in this version)

---

## 4. Third-party services

The App uses the following third-party services:

| Service | Purpose | Data sent |
|---|---|---|
| Google Gemini API | Primary input classification | Input text + context window (§3.2) |
| OpenAI API | Fallback classification when Gemini fails | Input text + context window (§3.2) |
| Railway | Hosting for the classification relay server | Request body (forwarded), access logs (§3.3) |
| Apple App Store | App distribution | Apple's standard distribution metadata |

Each provider's privacy policy:

- Google: <https://policies.google.com/privacy>
- OpenAI: <https://openai.com/policies/privacy-policy>
- Railway: <https://railway.com/legal/privacy>
- Apple: <https://www.apple.com/legal/privacy/>

---

## 5. Purpose of use

We use the collected information only for:

1. Classifying user input with AI and routing it to the right list or calendar
2. Storing entries in the on-device database so the user can view and edit them later
3. Investigating outages and detecting abuse via access logs

The Developer does **not** use the information for advertising, marketing, or sale to third parties.

---

## 6. Retention and deletion

- **On-device data**: deleted when the App is uninstalled. Individual data can also be deleted from the in-app Settings screen.
- **Server-side**: AI classification request bodies are not persisted. Railway access logs follow the provider's default retention.
- **Third-party AI**: Google and OpenAI retain data per their own policies (linked above).

---

## 7. Data export

The user can export all on-device data as JSON from the in-app Settings screen at any time.

---

## 8. Children's privacy

The App is not directed to children under the age of 13. If you are under 13, please do not use the App.

---

## 9. Security

- All communication with the classification server uses HTTPS.
- The server requires a shared-token authentication, preventing access from unexpected clients.
- The server does not persist user input, minimizing data-breach risk.

That said, no internet communication is perfectly secure. We recommend that you do not enter highly confidential information into the App.

---

## 10. Changes to this policy

If we change this policy, we will publish the updated version on this page with a new "Last updated" date. For material changes, we will also note the update in the App Store description.

---

## 11. Contact

For questions about this policy or to request deletion of your data, please contact:

**rrkhmd28@gmail.com**

---

[日本語版](./)
