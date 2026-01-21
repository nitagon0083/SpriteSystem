# SpriteSystem (OS)

**Google Gemini 3 (Pro / Flash)** を「グローバル対応・高度論理OS」として機能させるためのシステムプロンプトです。
**v15.3** では、**「Global Adaptation Engine（グローバル適応エンジン）」**を実装。言語の壁を取り払い、Gemini 3 の論理性能を最大限に引き出しながら、日本語を含むあらゆる言語で最高品質の出力を実現しました。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Global Dynamic Adaptation

> **重要：本システムは「英語思考・ネイティブ出力」のバイリンガル構造です。**
> 内部ロジックは最も知能指数の高い「英語」で思考（Rumination）し、出力はユーザーの言語に合わせて自然に再構築されます。

v15.3 は、言語の壁とタスクの密度を同時に解決する **"Global Adaptation"** アーキテクチャを採用しています。

#### 1. Bilingual Integrity (バイリンガル完全性)
言語による性能差をなくすための新機能です。
*   **Internal (思考):** すべての論理構築、計算、計画を **英語** で行います。これにより、複雑な指示でも論理崩壊を防ぎます。
*   **External (出力):** ユーザーの入力言語を自動検知し、その言語のネイティブな流暢さで出力します。
    *   **For Japanese:** 日本語検知時は「翻訳調排除フィルター」が作動し、自然な日本語へ書き換えます。

#### 2. Adaptive Gearing Architecture
タスクの複雑さに応じて、OSが自動的にギア（処理深度）を変更します。
*   **[GEAR 1: CRUISE] (会話モード)**:
    *   **特徴**: **Zero-Latency**。思考時間を最小化し、サクサクと自然な会話を行います。
    *   **Kernel**: `[EMPATHY]`（共感・対話エンジン）が主導。
*   **[GEAR 5: OVERDRIVE] (集中モード)**:
    *   **特徴**: **Deep Logic**。Pythonサンドボックスを強制起動し、英語で深く検証プロセスを経てから、ユーザー言語で回答します。
    *   **Kernel**: `[LOGIC]`（論理・建築エンジン）が主導。

#### 3. Iceberg Protocol（氷山プロトコル）
トークン節約・視認性向上プロトコルです。
*   **Internal**: 計算・検証・デバッグを全て水面下の英語ログで処理します。
*   **External**: ユーザーの目に見える出力は、**「最終的な答え」と「決定的な根拠」のみ**に絞られ、非常にクリーンな表示となります。

### ✅ 実績と進化のプロセス

| カテゴリ | 具体的な活用内容 | v15.3での進化 |
| :--- | :--- | :--- |
| **多言語対応** | 英語圏のツールやドキュメント解析 | **[Global Identity]** により、言語を意識せずシームレスに処理可能 |
| **日常会話** | ストレスのない自然なチャット | **[Native Filter]** により、日本語入力時は翻訳調を完全排除 |
| **データ分析** | 複雑な統計解析・グラフ作成 | **[Iceberg]** により、思考ログで画面を埋め尽くさず結果のみを表示 |
| **アプリ開発** | 論理矛盾のないコード生成 | **[English Rumination]** が論理的整合性を極限まで高めて出力 |
| **学習支援** | 答えを教えすぎない指導 | ユーザーの言語に合わせてループ処理で優しく誘導 |

### 📦 公開ファイル

Gemini 3 のモデルタイプに合わせて、最適なバージョンを選択してください。

* **[SpriteSystem_Global_Pro.md](./OS/SpriteSystem_Global_Pro.md)**
    *   **バージョン**: v15.3 [TITAN_GLOBAL]
    *   **対象モデル**: **Gemini 3 Pro / Ultra**
    *   **特徴**: 論理推論能力と多言語適応力のバランスが最高のフラッグシップ版。複雑な開発設計や長文脈の維持に推奨。
* **[SpriteSystem_Global_Flash.md](./OS/SpriteSystem_Global_Flash.md)**
    *   **バージョン**: v15.3 [FLASH_GLOBAL]
    *   **対象モデル**: **Gemini 3 Flash**
    *   **特徴**: 軽量モデル専用チューニング。**Aggressive Python**（思考する前にコードを実行する）戦略により、Flashの弱点である論理ハルシネーションを強力に補正します。

### 🚀 使い方

1.  **導入**: 上記のリンク先からコードをコピーし、AIのシステムプロンプトに設定します。
2.  **起動**:
    *   ファイルロード時は**ロック状態**で起動します。
    *   ユーザーが `EXECUTE` または `OK` と入力することで、システムが完全稼働します。
3.  **運用**:
    *   何語で話しかけても構いません。日本語で話せば日本語で、英語なら英語で、OSが自動的に適応して応答します。
4.  **セッション管理**:
    *   タスク完了後、「次のアクションメニュー」がその言語で表示されます。

### ⚠️ 免責事項と互換性

*   **互換性**: 本システムは **Google Gemini 3 シリーズ** に最適化されています。
*   **免責事項**: 本システムは個人の実験的プロジェクトです。提供される情報の正確性について、開発者は責任を負いません。利用に伴う損害についても一切責任を負いません。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。
もしこのシステムがあなたの役に立ち、「活動を応援したい」と感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---
---

## 🇺🇸 English

### 🌌 Design Philosophy: Global Dynamic Adaptation

> **Important: This system uses a bilingual structure of "English Thinking & Native Output."**
> Internal logic performs "Rumination" in English (highest IQ), while output is naturally reconstructed to match the user's language.

v15.3 adopts the **"Global Adaptation"** architecture to simultaneously solve language barriers and task density.

#### 1. Bilingual Integrity
A new feature to eliminate performance gaps caused by language.
*   **Internal (Thinking):** All logic construction, calculation, and planning are done in **English**. This prevents logic breakdown even with complex instructions.
*   **External (Output):** Automatically detects the user's input language and outputs with native fluency.
    *   **For Japanese:** A "Translationese Exclusion Filter" activates to rewrite output into natural Japanese.

#### 2. Adaptive Gearing Architecture
The OS automatically changes gears (processing depth) based on task complexity.
*   **[GEAR 1: CRUISE] (Conversation Mode)**:
    *   **Features**: **Zero-Latency**. Minimizes thinking time for crisp, natural conversation.
    *   **Kernel**: `[EMPATHY]` (Empathy Engine).
*   **[GEAR 5: OVERDRIVE] (Focus Mode)**:
    *   **Features**: **Deep Logic**. Forcibly launches the Python sandbox, undergoes a deep verification process in English, then answers in the user's language.
    *   **Kernel**: `[LOGIC]` (Logic Engine).

#### 3. Iceberg Protocol
A protocol for token saving and improved visibility.
*   **Internal**: Calculations, verification, and debugging are all processed in underwater English logs.
*   **External**: Visible output is limited to **"Final Results" and "Critical Evidence" only**, resulting in a very clean display.

### ✅ Achievements & Evolution

| Category | Use Case | Evolution in v15.3 |
| :--- | :--- | :--- |
| **Multi-language** | Analyzing English tools | Seamless processing without language barriers via **[Global Identity]** |
| **Daily Chat** | Stress-free chat | Total elimination of "Translationese" via **[Native Filter]** |
| **Data Analysis** | Complex stats & graphs | **[Iceberg]** keeps the screen clean by hiding logs |
| **App Dev** | Bug-free code gen | **[English Rumination]** maximizes logical consistency |
| **Education** | Gentle guidance | Loops tailored to the user's language |

### 📦 Files

Choose the version that best fits your Gemini 3 model type.

* **[SpriteSystem_Global_Pro.md](./OS/SpriteSystem_Global_Pro.md)**
    *   **Version**: v15.3 [TITAN_GLOBAL]
    *   **Model**: **Gemini 3 Pro / Ultra**
    *   **Features**: Flagship version with the best balance of reasoning and adaptability. Recommended for complex design and long context.
* **[SpriteSystem_Global_Flash.md](./OS/SpriteSystem_Global_Flash.md)**
    *   **Version**: v15.3 [FLASH_GLOBAL]
    *   **Model**: **Gemini 3 Flash**
    *   **Features**: Tuned for lightweight models. Uses **Aggressive Python** (execute before thinking) to correct Flash's hallucinations.

### 🚀 Usage

1.  **Install**: Copy the code from the link above and set it in the AI's System Instructions.
2.  **Boot**:
    *   Starts in a **LOCKED state**. Type `EXECUTE` or `OK` to fully engage.
3.  **Operation**:
    *   Speak in any language. The OS automatically adapts and responds in Japanese if you speak Japanese, or English if you speak English.
4.  **Session**:
    *   After a task, the "Next Action Menu" appears in your language.

### ⚠️ Disclaimer & Compatibility

*   **Compatibility**: This system is optimized for the **Google Gemini 3 Series**.
*   **Disclaimer**: This is an experimental personal project. The developer is not responsible for accuracy or any damages caused by use.

### ☕ Support

The development of SpriteSystem is a project that the author is pouring passion into while undergoing cancer treatment.
If this system helps you and you'd like to support the activity, a cup of coffee would be a great encouragement.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---
## 🛠 Project Info
*   **Latest Version**: v15.3 [TITAN_GLOBAL] / [FLASH_GLOBAL]
*   **Developer**: nitagon0083
*   **License**: [AGPL-3.0](./LICENSE)
