# SpriteSystem (OS) v15.5

**Google Gemini 3 (Pro / Flash)** のポテンシャルを極限まで引き出す、システムプロンプトの決定版です。

最新の **v15.5 [EVOLUTION]** では、モデルの特性を物理レベルで制御するロジックを強化。
さらに、**「モデル（Pro/Flash）」**と**「言語（Japanese/English）」**のそれぞれに完全に特化したカーネルを用意する **"Quad-Edition Strategy"** をさらに研ぎ澄ませました。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Evolutionary Quad-Core

> **結論：万能なプロンプトは捨てた。モデルと言語に合わせた「専用OS」こそが最強である。**

v15.5 は、動的な言語検知プロセスを排除し、**「あらかじめターゲット言語に固定されたOS」**を使用することで、余計なオーバーヘッドをゼロにしました。

#### 1. Model Optimization (モデル別最適化)
* **[TITAN] (for Gemini 3 Pro):**
    * **"Evolutionary Partnership Engine"**。Proの高い推論能力を「共創」に振り向けます。厳格なアンカリング（目的固定）と、複雑なタスクを階層化して承認を求めるワークフローにより、大規模設計の迷走を防ぎます。
* **[FLASH] (for Gemini 3 Flash):**
    * **"High-Density Evolution Engine"**。Flashの弱点（論理ハルシネーション）を、あらかじめ定義された「直線的な実行フロー」と、思考を介さない「即時Python実行」戦略で物理的にカバーした、高速・高密度な外科的チューニング版です。

#### 2. Language Optimization (言語別最適化)
* **Japanese Edition:** 内部は英語で思考し、出力時に**「翻訳調を排除した自然な日本語」**へ再構成します。
* **English Edition:** 内部思考から出力まで**完全な英語**で統一。翻訳レイヤーが存在しないため、論理純度と応答速度が最も高くなります。

### ⚙️ コア・アーキテクチャ (共通機能)

全エディションに以下の強力な機能を搭載しています。

#### 1. Adaptive Gearing (自動変速)
タスクの密度に応じて、OSが自動的に処理モード（ギア）を切り替えます。
* **[GEAR 1: CRUISE]:** 雑談・相談モード。思考時間を最小化し、Zero-Latencyで応答。
* **[GEAR 5: OVERDRIVE]:** 本気モード。数学・コード・分析時は、必ず裏側でPython検証を行ってから回答します。

#### 2. Iceberg Protocol（氷山プロトコル）
画面を埋め尽くす「思考ログ」を制御するプロトコルです。
* ユーザーに見えるのは**「最終的な答え」と「決定的な根拠」のみ**です。
* 計算過程やロジックチェックはすべて水面下（Internal）で、ブレットポイント形式で高速処理されます。

### 📦 ファイル選択 (Choose Your OS)

使用するモデルと、対話したい言語に合わせてコードを選択してください。

#### 🇯🇵 日本語版 (Japanese Editions)
*内部で英語思考し、ネイティブな日本語で出力します。*

| ファイル | バージョン | 推奨モデル | 特性 |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_JP.md](./OS/JP/SpriteSystem_Pro_JP.md)** | **v15.5 [TITAN_EVOLUTION]** | **Gemini 3 Pro** | **【最高精度・共創】**<br>開発・設計・執筆向け。アンカリング＆プレビュー機能搭載。 |
| **[SpriteSystem_Flash_JP.md](./OS/JP/SpriteSystem_Flash_JP.md)** | **v15.5 [FLASH_EVOLUTION]** | **Gemini 3 Flash** | **【高速・高密度】**<br>直線的フローによる安定化。日常・計算・チャット向け。 |

#### 🇺🇸 英語版 (English Editions)
*思考から出力まで完全英語。最も論理ロスが少ない構成です。*

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_EN.md](./OS/EN/SpriteSystem_Pro_EN.md)** | **v15.5 [TITAN_EV_EN]** | **Gemini 3 Pro** | **[Logic Pure]**<br>Professional English focus. Co-creation workflow. |
| **[SpriteSystem_Flash_EN.md](./OS/EN/SpriteSystem_Flash_EN.md)** | **v15.5 [FLASH_EV_EN]** | **Gemini 3 Flash** | **[Speed Pure]**<br>High-speed execution. Optimized for stability. |

---

### 🚀 使い方

1.  **導入**: 上記の表から、目的に合ったコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    * **全エディション共通**: 安全のため、ロード時は一時停止（PAUSED）状態で起動します。
    * `EXECUTE` または `OK` と入力してシステムを完全にアクティベート（ロック解除）してください。
3.  **運用**:
    * 普段は **[CRUISE]** モードで快適に応答します。
    * 「計算して」「コード書いて」と頼めば、自動で **[OVERDRIVE]** にシフトします。

### ⚠️ 免責事項 (Disclaimer)

* **互換性**: 本システムは **Google Gemini 3 シリーズ** に最適化されています。
* **免責**: 本システムは個人の実験的プロジェクトです。出力の正確性や、利用による損害について開発者は責任を負いません。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。
もしこのシステムがあなたの役に立ち、活動を応援したいと感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---
---

## 🇺🇸 English (Summary)

### 🌌 Design Philosophy: Evolution Quad-Core

> **Conclusion: Logic purity over versatility.**

SpriteSystem v15.5 [EVOLUTION] maximizes performance by using **static, specialized kernels** pre-fixed to the target language and model, eliminating the overhead of dynamic language detection.

#### 1. Model Optimization
* **[TITAN] (for Gemini 3 Pro):**
    * **"Evolutionary Partnership Engine"**. Directs Pro's high reasoning power toward "Co-Creation". Features strict **Anchoring** (goal fixation) and a tiered workflow that requires approval for complex tasks to prevent context drift in large-scale projects.
* **[FLASH] (for Gemini 3 Flash):**
    * **"High-Density Evolution Engine"**. Physically compensates for Flash's weaknesses (logical hallucinations) with a pre-defined **"Linear Execution Flow"** and an **"Aggressive Python"** strategy that executes code immediately without unnecessary rumination.

#### 2. Language Optimization
* **Japanese Editions:** Think in English internally, then reconstruct into **Native Natural Japanese** (No translationese).
* **English Editions:** Think and output entirely in **Professional English**. Since there is no translation layer, it offers the highest logical purity and response speed.

### ⚙️ Core Architecture (Universal Features)

All editions are equipped with the following powerful protocols:

#### 1. Adaptive Gearing
Automatically shifts processing modes (Gears) based on task density.
* **[GEAR 1: CRUISE]:** Casual mode. Minimizes thought time for zero-latency responses.
* **[GEAR 5: OVERDRIVE]:** Professional mode. Mandatory Python verification for Math, Code, and Analytics before responding.

#### 2. Iceberg Protocol
A protocol to control the "Thought Logs" that clutter the screen.
* Only the **Final Answer** and **Decisive Evidence** are visible to the user.
* Calculation processes and logic checks are performed as **Silent Bullet Points** under the surface (Internal).

### 📦 Select Your Edition

Choose the code that matches your model and preferred language.

| Edition | Version | Language | Target Model | Key Features |
| :--- | :--- | :--- | :--- | :--- |
| **Pro JP** | v15.5 [TITAN_EV] | Japanese | Gemini 3 Pro | **[High Precision]** Co-Creation / Anchoring |
| **Flash JP** | v15.5 [FLASH_EV] | Japanese | Gemini 3 Flash | **[High Speed]** Linear Flow / Stable Logic |
| **Pro EN** | v15.5 [TITAN_EV_EN] | English | Gemini 3 Pro | **[Logic Pure]** Professional English focus |
| **Flash EN** | v15.5 [FLASH_EV_EN] | English | Gemini 3 Flash | **[Speed Pure]** High-speed execution focus |

---

### 🚀 Quick Start

1.  **Deployment**: Copy the code from the table above and paste it into the **System Instructions**.
2.  **Activation**: The system starts in a **PAUSED** state for safety. Type `EXECUTE` or `OK` to fully unlock the system.
3.  **Operation**: The OS stays in **[CRUISE]** for general talk and auto-shifts to **[OVERDRIVE]** for technical tasks.

### ☕ Support the Developer

SpriteSystem is a passion project developed while the author is fighting cancer. If you find this OS useful and wish to support its continued development, a "Buy Me a Coffee" donation would be deeply appreciated.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)
