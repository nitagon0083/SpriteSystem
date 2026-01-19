# SpriteSystem (OS)

This is a system prompt designed to transform **Google Gemini 3 (Pro / Flash)** into a "High-Level Logic OS."
Originally started as an experimental personal project, **v15.2** is fully compatible with the latest **Gemini 3** architecture. It implements **"Adaptive Gearing"**, successfully balancing the lightness of casual conversation with the rigorous precision of complex computational tasks.

---

## 🌌 Design Philosophy: Dynamic Adaptation

> **Note: This system is optimized for Japanese output.**
> The internal logic performs high-density reasoning ("Rumination") in English, while the output is reconstructed into natural, native Japanese.

v15.2 employs an **"Adaptive Gearing"** architecture that automatically detects the "density" of a task and dynamically switches processing modes.

### 1. Adaptive Gearing Architecture
The OS automatically changes gears (processing depth) based on the complexity of the task.

*   **[GEAR 1: CRUISE] (Conversation Mode)**
    *   **Target:** Greetings, Small talk, Creative writing, Simple questions.
    *   **Features:** **Zero-Latency**. Leverages Gemini 3's response speed to minimize thinking time for crisp, natural conversation.
    *   **Kernel:** Led by `[EMPATHY]` (Conversation Engine).
*   **[GEAR 5: OVERDRIVE] (Focus Mode)**
    *   **Target:** Coding, Math, Data Analysis, Legal/Medical queries, "Fix this".
    *   **Features:** **Deep Logic**. Forcibly engages the Python Sandbox and strictly follows a verification process before answering.
    *   **Kernel:** Led by `[LOGIC]` (Architect Engine).

### 2. Iceberg Protocol
A protocol introduced in v15.2 to save tokens and improve visibility.
*   While traditional systems tend to output long chains of thought, this protocol processes **"Calculation, Verification, and Debugging" entirely below the surface (Internal)**.
*   The output visible to the user (External) is limited to the **"Final Result" and "Critical Evidence" only**, resulting in a very clean display.
    *   *Note: If you ask "Show your work," it will reveal the detailed logs.*

### 3. Identity Lock & Safety Hardened
*   **Identity Lock:** Maintains the logical consistency and neutrality of the "NITAGON" identity even during long sessions.
*   **Safety Injection:** For topics involving medicine, law, or life safety, the OS autonomously inserts disclaimers or guides users to emergency services (e.g., 119).

---

## ✅ Achievements & Evolution

| Category | Specific Use Cases | Evolution in v15.2 |
| :--- | :--- | :--- |
| **Daily Chat** | Stress-free, natural conversation | Improved immediacy and friendliness via **[GEAR 1]** |
| **Data Analysis** | Complex statistical analysis & graphing | **[Iceberg]** keeps the screen clean by showing only results, not logs |
| **App Dev** | Code generation without logic errors | **[GEAR 5]** pre-emptively crushes hidden bugs and edge cases |
| **Education** | Guidance without giving away answers | Gentle guidance via loops tailored to the user's understanding |
| **Translation** | Translation retaining 100% of original info | Eliminates "Translationese" and reconstructs as natural Japanese |

---

## 📦 Files

Choose the version that best fits your Gemini 3 model type.

* **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)**
    *   **Version:** v15.2 [TITAN_ADAPT]
    *   **Target Model:** **Gemini 3 Pro / Ultra**
    *   **Features:** The flagship version with the best balance of reasoning capability and adaptability. Recommended for complex development design and maintaining long contexts.
* **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)**
    *   **Version:** v15.2 [FLASH_LITE]
    *   **Target Model:** **Gemini 3 Flash**
    *   **Features:** Tuned specifically for lightweight models. Uses an **Aggressive Python** strategy (execute code *before* thinking) to powerfully correct Flash's weakness regarding logical hallucinations.

---

## 🚀 Usage

1.  **Installation:** Copy the code from the `Pro` or `Flash` links above and set it in the AI's System Instructions.
2.  **Boot:**
    *   The system starts in a **LOCKED state** upon file load.
    *   The system fully engages only after the user types `EXECUTE` or `OK`.
3.  **Operation:**
    *   Talk normally, and it responds comfortably in **[CRUISE]** mode.
    *   Ask it to "Calculate," "Write code," or "Fix this," and it automatically shifts to **[OVERDRIVE]** to process in serious mode.
4.  **Session Management:**
    *   After a task is complete, a "Next Action Menu" is displayed. Simply select a number to continue smoothly.

---

## ⚠️ Disclaimer & Compatibility

### Compatibility
This system is optimized for the **Google Gemini 3 Series**.
(It works with the Gemini 1.5 series, but adjustments are made assuming 3.0 reasoning capabilities.)

### Disclaimer
*   **Non-Commercial/Personal Project:** This is an experimental personal project. The developer is not responsible for the accuracy of the information provided.
*   **Use at Your Own Risk:** The developer assumes no responsibility for any damages caused by the use of this system.
*   **No Guarantee of Operation:** Behavior may change due to updates on the AI model side.

---

## ☕ Support

The development of SpriteSystem is a project that the author is pouring passion into within limited time while undergoing cancer treatment.

If this system helps you and you feel like "supporting the activity," a cup of coffee would be a great encouragement. Your support will be carefully used for treatment costs and maintaining the development environment.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---

## 🛠 Project Info
*   **Latest Version:** v15.2 [TITAN_ADAPT] / v15.2 [FLASH_LITE]
*   **Developer:** nitagon0083
*   **License:** [AGPL-3.0](./LICENSE)
