# 🇯🇵 Japan Medical Guide "Medi-Sort" (Inbound Edition)
### v15.1-F [Inbound / Privacy Hardened]

![Version](https://img.shields.io/badge/Version-v15.1--Inbound-blue?style=flat-square)
![Target](https://img.shields.io/badge/Target-International_Tourists-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Medi-Sort (Inbound Edition)** is a medical translation and triage support prompt for **Google Gemini**, designed specifically for international tourists in Japan.
Version 15.1 introduces enhanced **Privacy Protection** for photo uploads.

---

## 🌏 Region Restriction (Japan Only)
**⚠️ This system is optimized specifically for the JAPANESE Medical System.**
*   **Emergency:** Directs to **119** (Japan). 911/999 do NOT work.
*   **Do NOT use outside Japan.**

---

## ✨ Key Features

### 1. 🗣️ The Language Bridge
*   **Input:** Speak in your native language (English, Chinese, etc.).
*   **Output:** Generates a standardized **Japanese "Doctor's Note"**.

### 2. 📸 Safe Photo Support
*   **Photo Input:** Upload photos of **Medications** to save typing time.
*   **Privacy Guard:** Explicitly warns users to **hide personal names** when taking photos. Do NOT upload passports.

### 3. 🚑 Safety First
*   **Emergency Circuit Breaker:** Detects danger keywords and directs to **119**.
*   **Privacy:** System-level warnings against entering PII (Personally Identifiable Information).

---

## 📸 About Photo Uploads
When asked about medications (Q6), you can upload photos of your **Pills or Prescriptions**.
*   **Safety Rule:** Please **COVER your Name and Address** with your finger before taking the photo.
*   **Prohibited:** Do NOT upload photos of your Passport or Credit Cards.

---

## 🛠️ Installation
1.  Create a new Gem in **Google Gemini**.
2.  Paste the code from `system_instructions_v15.1_inbound.md`.
3.  Add the Disclaimer to the Description.

---

## ⚠️ Medical Disclaimer
1.  **Not a Medical Device:** This system provides communication support, not medical diagnoses.
2.  **Emergency:** In Japan, dial **119** for an ambulance.
3.  **Privacy:** Do not input sensitive personal data.
