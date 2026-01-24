# SpriteSystem (OS)

**Google Gemini 3 (Pro / Flash)** のポテンシャルを極限まで引き出す、日本語ユーザーのための「二層構造アーキテクチャ」システムプロンプトです。

実験的な **v15.3 (Global)** での運用結果（汎用化による論理精度の希釈）を踏まえ、本プロジェクトは **最も評価の高かった v15.2 ベース** へと回帰しました。
さらに、**Gemini 3 Pro** と **Flash** それぞれの「思考の癖」に合わせてカーネルを物理的に分割・最適化する **"Dual-Edition Strategy"** を採用しています。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Titan & Flash Optimization

> **結論：万能なプロンプトは存在しない。モデルに合わせた「専用OS」が必要である。**

v15.2 は、**「英語で思考し、日本語で出力する」** というバイリンガル構造を核としています。
Gemini 3 のモデルごとの特性に合わせて、以下の2つのエディションを用意しました。

#### 1. [TITAN_ADAPT] Edition (for Pro)
*   **対象:** **Gemini 3 Pro / Ultra**
*   **哲学:** **"Deep Logic & Strict Control"**
*   **特徴:**
    *   Proの高い推論能力を活かし、**長文の英語思考（Rumination）** を強制します。
    *   **Strict Lock:** ファイル読み込み時は機能を完全にロックし、ユーザーの許可があるまで動き出しません。これにより、指示の読み飛ばしを防ぎます。
    *   複雑なコーディング、要件定義、物語作成において、圧倒的な整合性を発揮します。

#### 2. [FLASH_ADAPT] Edition (for Flash)
*   **対象:** **Gemini 3 Flash**
*   **哲学:** **"Direct-Stream & Aggressive Python"**
*   **特徴:**
    *   Flash特有の「考えすぎてフリーズする」「論理が上滑りする」弱点を克服するための外科的チューニング版です。
    *   **Bullet Point Thinking:** 思考プロセスを箇条書きに限定し、メモリ消費とタイムアウトを防ぎます。
    *   **Aggressive Python:** 計算や論理パズルにおいて、「考える前にコードを実行する」戦略を強制。Flashのハルシネーション（計算ミス）を物理的に封じ込めます。
    *   **Gatekeeper Paused:** 厳格すぎるロックを緩和し、スムーズな立ち上がりを重視しています。

---

### ⚙️ コア・アーキテクチャ (共通機能)

両エディションともに、以下の強力な機能（Adaptive Gearing）を搭載しています。

#### 1. Adaptive Gearing (自動変速)
タスクの密度に応じて、OSが自動的に処理モードを切り替えます。

*   **[GEAR 1: CRUISE] (会話モード)**
    *   **対象:** 挨拶、雑談、簡単な質問。
    *   **挙動:** **Zero-Latency**。思考時間を最小化し、サクサクと自然な会話を行います。
    *   **Kernel:** `[EMPATHY]`（共感エンジン）主導。
*   **[GEAR 5: OVERDRIVE] (集中モード)**
    *   **対象:** 数学、データ分析、複雑なコード修正、"Fix this"。
    *   **挙動:** **Mandatory Python**。裏側で必ずPythonサンドボックスを起動し、検証を行ってから回答します。
    *   **Kernel:** `[LOGIC]`（論理エンジン）主導。

#### 2. Iceberg Protocol（氷山プロトコル）
画面を埋め尽くす「思考ログ」を制御するプロトコルです。
*   **Internal:** 計算、検証、デバッグはすべて水面下で行います。
*   **External:** ユーザーに見えるのは**「最終的な答え」と「決定的な根拠」のみ**です。
*   これにより、モバイル端末でも快適な視認性を確保しています。

#### 3. Bilingual Integrity（バイリンガル完全性）
*   **思考（Internal）:** 論理IQが最も高くなる **English** で行います。
*   **出力（External）:** ユーザーに対しては、翻訳調を排除した **Native Natural Japanese** で出力します。

---

### 📦 ファイル選択 (Choose Your OS)

使用するモデルに合わせて、コードを選択してください。

| ファイル | バージョン | 推奨モデル | 特性 |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)** | **v15.2 [TITAN_ADAPT]** | **Gemini 3 Pro / Ultra** | **【最高精度・厳格】**<br>重厚な論理思考と厳格な制御。複雑なタスク向け。 |
| **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)** | **v15.2 [FLASH_ADAPT]** | **Gemini 3 Flash** | **【高速・安定】**<br>計算ミス防止機能(Aggressive Python)搭載。レスポンス重視。 |

### 🚀 使い方

1.  **導入**: 上記のリンク先から、モデルに合ったコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    *   **Pro版**: ロック状態で起動します。`EXECUTE` または `OK` と入力してロックを解除してください。
    *   **Flash版**: 待機状態で起動します。すぐに会話を始められます。
3.  **運用**:
    *   普段は **[CRUISE]** モードで快適に応答します。
    *   「計算して」「コード書いて」と頼めば、自動で **[OVERDRIVE]** にシフトします。

### ⚠️ 免責事項 (Disclaimer)

*   **互換性**: 本システムは **Google Gemini 3 シリーズ** に最適化されています。他モデル（GPT-4等）では意図した動作をしない可能性があります。
*   **免責**: 本システムは個人の実験的プロジェクトです。出力の正確性や、利用による損害について開発者は責任を負いません。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。

もしこのシステムがあなたの役に立ち、「活動を応援したい」と感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。頂いた支援は、治療費や開発環境の維持に大切に使わせていただきます。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

### 🛠 プロジェクト情報
*   **Current Version**: v15.2 [TITAN_ADAPT] / v15.2 [FLASH_ADAPT]
*   **Developer**: nitagon0083
*   **License**: [AGPL-3.0](./LICENSE)

---
---

## 🇺🇸 English (Summary)

### 🌌 Design Philosophy: Return to Precision

> **Conclusion: We reverted from v15.3 (Global) back to v15.2 to prioritize logical density and Japanese output quality.**

SpriteSystem v15.2 adopts a **"Dual-Edition Strategy"** to maximize the potential of Gemini 3 Pro and Flash respectively.

#### 1. [TITAN_ADAPT] Edition (for Pro)
*   **Target:** **Gemini 3 Pro / Ultra**
*   **Focus:** **Deep Logic & Strict Control.**
*   It enforces deep English rumination and strict gatekeeping to ensure maximum logical consistency for complex tasks.

#### 2. [FLASH_ADAPT] Edition (for Flash)
*   **Target:** **Gemini 3 Flash**
*   **Focus:** **Direct-Stream & Aggressive Python.**
*   A surgically tuned version to fix Flash's weaknesses (hallucinations/freezing). It uses "Bullet Point Thinking" for speed and "Aggressive Python" to force code execution for math/logic.

### 📦 Files

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)** | **v15.2 [TITAN_ADAPT]** | **Gemini 3 Pro** | **High Precision.** Strict logic & detailed English thinking. |
| **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)** | **v15.2 [FLASH_ADAPT]** | **Gemini 3 Flash** | **High Speed.** Stabilized logic with Aggressive Python. |

### 🚀 Usage

1.  Copy the code from the link above corresponding to your model.
2.  Paste it into the System Instructions.
3.  **Pro:** Type `EXECUTE` to unlock. **Flash:** Ready to go immediately.
4.  The system automatically switches between **[CRUISE]** (Chat) and **[OVERDRIVE]** (Logic/Code) modes.

*(See Japanese section for Support & Disclaimer)*
