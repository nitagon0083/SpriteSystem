# SpriteSystem

**SpriteSystem** is a system prompt designed to make Google Gemini function as an "AI OS".
It is an experimental project developed by an individual enthusiast, aimed at maximizing the AI's inherent logical capabilities and achieving "Zero-Loss" information preservation.

In **v15.0**, the system has evolved into a **"Dual-Kernel" Architecture**, integrating flexible dialogue and safety features alongside its traditional powerful logic engine.

---

## 🌌 Design Philosophy

> **Note: This system is optimized for processing in Japanese.**
> The internal logic is constructed in English to maximize reasoning density, but the output is tuned to perform best in a Japanese environment. (You may need to modify the `[LEVEL 0]` section for English-only output).

The system is built on three core pillars:

### 1. Dual-Kernel Architecture
> **"Coexistence of Cold Logic and Warm Empathy"**
The system instantly analyzes the nature of the task and dynamically switches between two personality kernels.
*   **[KERNEL: LOGIC]**: The traditional TITAN specification. Cold, high-speed logical processing for code generation and mathematics.
*   **[KERNEL: EMPATHY]**: The new dialogue engine. Gentle, polite guidance and sequential verification for beginners and consultation tasks.

### 2. "Cognitive Brake" for Hallucination Control
To prevent the "rushing" (hallucinations/jumping to conclusions) characteristic of high-speed models like Flash, an OS-level **"Anti-Rush Protocol"** has been implemented.
For ambiguous instructions, the system uses a **Sequential Loop** to guide the user to the goal one step at a time instead of answering everything at once.

### 3. LogicGrid Engine for Logical Consistency
Ambiguity is eliminated by enforcing step-by-step verification. For critical tasks (debugging, mathematical proofs), the system incorporates **"The Sudoku Standard,"** automatically executing Python to ensure objective accuracy.

---

## ✅ Track Record & Evolution

The developer has verified practicality in the following tasks. Precision is continuously polished through a "feedback loop" of insights gained from actual use.

| Category | Specific Use Cases | Evolution in v15.0 |
| :--- | :--- | :--- |
| **App Development** | Zero-Loss code generation without logical contradictions | Strict specification adherence via Logic Kernel |
| **Medical/Consulting** | Hearing symptoms/concerns, organizing facts | **[NEW]** Listening & safety nets via Empathy Kernel |
| **Data Analysis** | Precision statistics/graphing via Python execution | Improved autonomous self-correction on errors |
| **Tutoring** | Step-by-step guidance without giving away answers | **[NEW]** Understanding checks via Sequential Loop |
| **Writing** | Precision translation/rewriting maintaining 100% nuance | Dynamic tone switching based on context |

---

## 📦 Public Files

You can get the latest versions from the files in the repository.

*   **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)**
    *   **Version**: v15.0 [TITAN_NEXUS]
    *   **Recommended For**: Advanced tasks (Development, Deep Logic, Complex Consulting)
    *   **Features**: The flagship model with "Dual-Kernel" switching between Logic and Empathy.
*   **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)**
    *   **Version**: v15.0-F [FLASH_NEXUS]
    *   **Recommended For**: Daily tasks, Mobile use, Token saving
    *   **Features**: Enhanced "Cognitive Brake". Suppresses the rushing of high-speed models to ensure reliable dialogue.

---

## 🚀 How to Use

1.  **Installation**: Copy the code from `Pro` or `Flash` linked above and set it as the AI's System Instructions.
2.  **Boot**: When the OS loads successfully, the AI will respond with **`System Ready...`** and enter standby mode.
3.  **Operation**:
    *   **For Development**: Command `Create...`, `Fix...`, etc. The system immediately engages **[LOGIC]** mode for high-speed processing.
    *   **For Consultation**: Say `Help...`, `Guide...`, etc. The system engages **[EMPATHY]** mode for gentle hearing.
4.  **Session Management**:
    *   After a task is complete, the AI displays a "Next Action Menu" (Edit/New/Finish). You can smoothly continue by simply selecting a number.

---

## ⚠️ Disclaimer & Compatibility

### Compatibility
This system is optimized for the Google Gemini series (3 Pro / Flash).

> **Note**: While the design philosophy may be applicable to other LLMs (Claude, GPT-4, etc.), operation is not guaranteed due to differences in model characteristics. Porting to other models is at your **own risk**.

### Disclaimer
*   **Non-Commercial / Personal Project**: This system is an experimental personal project. The developer bears no responsibility for the accuracy, completeness, or usefulness of the information provided.
*   **Self-Responsibility**: The developer bears no responsibility for any damages (direct or indirect) resulting from the use of this system or prompt. Please use it at your own risk.
*   **No Guarantee of Operation**: Intended behaviors or protocols may be maintained due to AI model updates, etc.

---

## ☕ Support Development

The development of SpriteSystem is a project poured with passion within limited time while the author undergoes cancer treatment.

If you find this system useful and would like to support the activity, buying a coffee would be a great encouragement. Your support will be carefully used for treatment costs and maintenance of the development environment.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---

## 🛠 Project Info
*   **Latest Version**: v15.0 [TITAN_NEXUS] / v15.0-F [FLASH_NEXUS]
*   **Developer**: nitagon0083
*   **License**: [AGPL-3.0](./LICENSE)
