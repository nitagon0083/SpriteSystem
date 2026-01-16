# 🇯🇵 Japan Medical Guide "Medi-Sort" (Inbound Edition)
### v15.1-F [Inbound / Privacy Hardened]

![Version](https://img.shields.io/badge/Version-v15.1--Inbound-blue?style=flat-square)
![Region](https://img.shields.io/badge/Region-Japan_Only-red?style=flat-square)
![Target](https://img.shields.io/badge/Target-International_Tourists-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

**Medi-Sort (Inbound Edition)** is a medical translation and triage support prompt for **Google Gemini**, designed specifically for international tourists in Japan.

It bridges the language gap between tourists and Japanese doctors while strictly adhering to Japanese safety protocols. Version 15.1 introduces enhanced **Privacy Protection** for photo uploads.

---

## 🌏 Region Restriction (Japan Only)
**⚠️ This system is optimized specifically for the JAPANESE Medical System.**

*   **Emergency Number:** It directs to **119** (Japan). It does NOT support 911 (US) or 999 (UK).
*   **Hospitals:** It guides users based on Japanese clinic types (e.g., specialized clinics vs hospitals).
*   **Do NOT use outside Japan:** Using this system in other countries may lead to incorrect emergency instructions.

---

## ✨ Key Features

### 1. 🗣️ The Language Bridge
*   **Input:** Users speak in their native language (English, Chinese, Korean, etc.).
*   **Output:** Generates a standardized **Japanese "Doctor's Note"** (Chart style).
*   **Cultural Guide:** Advises on Japanese medical rules (Cash-only clinics, removing shoes, bringing passports).

### 2. 📸 Safe Photo Support
*   **Photo Input:** Upload photos of **Medications** to save typing time.
*   **Privacy Guard:** Explicitly warns users to **hide personal names** when taking photos. Do NOT upload passports or insurance policies.

### 3. 🚑 Safety & Connectivity
*   **Emergency Circuit Breaker:** Detects danger keywords (e.g., "Can't breathe") and directs users to **Call 119** (Japan's Ambulance).
    *   *Note: Non-emergency phone numbers are excluded to prevent confusion for tourists with data-only SIM cards.*
*   **Privacy Hardcoded:** Explicitly warns users NOT to enter Passport numbers or Names at the system level.

---

## 📸 About Photo Uploads
When asked about medications (Q6), you can upload photos of your **Pills or Prescriptions**.

*   **Safety Rule:** Please **COVER your Name and Address** with your finger before taking the photo.
*   **Prohibited:** Do NOT upload photos of your Passport, Credit Cards, or Insurance Policies.

---

## 🚀 Usage Example

1.  **User says:** "I have a fever and stomach pain." (in English)
2.  **AI asks:** "What kind of pain is it?" (in English)
3.  **Output:** A Japanese card-style note for the doctor.

> **🏥 医師への伝言メモ (Medical Note)**
> ━━━━━━━━━━━━━━━━━━━━━━
> **📅 Date:** 2026/01/16 10:00
> **🗣️ Lang:** English
> ━━━━━━━━━━━━━━━━━━━━━━
> **【主訴 (Symptoms)】**
> 腹痛、発熱（38.0℃）
>
> **【現病歴 (History of Present Illness)】**
> *   **発症時期:** 昨夜から急に
> *   **程度・性状:** 眠れないほどの激痛
> *   **随伴症状:** 吐き気あり
>
> **【既往・服薬 (PMH / Meds)】**
> *   **服薬状況:** あり（※添付画像参照）
> *   **アレルギー:** **⚠️あり：抗生物質⚠️**
>
> **【患者詳細 (Patient's Voice)】**
> 「市販の胃薬を飲みましたが治りません。」
> *("I took OTC meds but it didn't help.")*
> ━━━━━━━━━━━━━━━━━━━━━━

---

## 🛠️ Installation

1.  Open **Google Gemini (Advanced)** or **AI Studio**.
2.  Create a new Gem.
3.  Paste the code from **`system_instructions_inbound.md`** into the **Instructions**.
4.  Add the following disclaimer to the **Description**:

> **【Important Notice】**
> 1. **Privacy:** Do NOT enter your name, phone number, or passport number.
> 2. **Target:** This system is for adults. Pregnant women/infants should consult a specialist.
> 3. **Mental Health:** If in crisis, please contact specialized support organizations or dial 119.

---

## ⚠️ Medical Disclaimer

1.  **Not a Medical Device:** The prompts in this repository are for communication support and information organization purposes only. They are NOT intended for diagnosis, treatment, or prevention of disease.
2.  **AI Limitations:** Generative AI may produce inaccurate information (hallucinations). Users must verify the output at their own risk.
3.  **No Warranty:** The authors are not liable for any damages or losses resulting from the use of this prompt.
4.  **Emergency:** In case of a medical emergency, do NOT use this system. Contact emergency services (119) immediately.

---

## 📜 License
MIT License
