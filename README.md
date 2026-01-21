# SpriteSystem (OS) v15.3

**Google Gemini 3 (Pro / Flash)** を「グローバル対応・高度論理OS」として機能させるためのシステムプロンプトです。
実験的なプロジェクトとしてスタートしましたが、**v15.3** では最新の **Gemini 3** アーキテクチャに完全対応。**「Global Adaptation（グローバル適応）」**と**「Adaptive Gearing（適応型ギア変速）」**を実装し、言語の壁を超えて日常会話の軽快さと演算処理の厳密さを両立させることに成功しました。

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

*   **[GEAR 1: CRUISE] (会話モード)**
    *   **対象**: 挨拶、雑談、創作、簡単な質問など。
    *   **特徴**: **Zero-Latency**。Gemini 3 の応答速度を活かし、思考時間を最小化してサクサクと自然な会話を行います。
    *   **Kernel**: `[EMPATHY]`（共感・対話エンジン）が主導。
*   **[GEAR 5: OVERDRIVE] (集中モード)**
    *   **対象**: コーディング、数学、データ分析、法的/医学的質問、"Fix this"。
    *   **特徴**: **Deep Logic**。Pythonサンドボックスを強制起動し、英語で深く検証プロセスを経てから、ユーザー言語で回答します。
    *   **Kernel**: `[LOGIC]`（論理・建築エンジン）が主導。

#### 3. Iceberg Protocol（氷山プロトコル）
v15.2 で導入されたトークン節約・視認性向上プロトコルです。
*   従来のシステムでは思考過程が長文で出力されがちでしたが、本プロトコルでは**「計算・検証・デバッグ」を全て水面下（Internal）で処理**します。
*   ユーザーの目に見える出力（External）は、**「最終的な答え」と「決定的な根拠」のみ**に絞られ、非常にクリーンな表示となります。
    *   *※「計算過程を見せて」と頼めば、詳細ログを開示します。*

#### 4. Global Identity & Safety Hardened
*   **Identity Lock**: 長時間のセッションでも「NITAGON」としての論理整合性と中立性を維持します。
*   **Safety Injection**: 医療・法律・生命に関わるトピックでは、OSが自律的に免責事項を挿入、または緊急通報（119/911等）への誘導を行います。

### ✅ 実績と進化のプロセス

| カテゴリ | 具体的な活用内容 | v15.3での進化 |
| :--- | :--- | :--- |
| **日常会話** | ストレスのない自然なチャット | **[Native Filter]** により、日本語入力時は翻訳調を完全排除 |
| **データ分析** | 複雑な統計解析・グラフ作成 | **[Iceberg]** により、思考ログで画面を埋め尽くさず結果のみを表示 |
| **アプリ開発** | 論理矛盾のないコード生成 | **[English Rumination]** が論理的整合性を極限まで高めて出力 |
| **学習支援** | 答えを教えすぎない指導 | ユーザーの言語に合わせてループ処理で優しく誘導 |
| **多言語対応** | 英語圏ツールの解析・翻訳 | **[Global Identity]** により、言語を意識せずシームレスに処理可能 |

### 📦 公開ファイル

Gemini 3 のモデルタイプに合わせて、最適なバージョンを選択してください。

* **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)**
    *   **バージョン**: v15.3 [TITAN_GLOBAL]
    *   **対象モデル**: **Gemini 3 Pro / Ultra**
    *   **特徴**: 論理推論能力と多言語適応力のバランスが最高のフラッグシップ版。複雑な開発設計や長文脈の維持に推奨。
* **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)**
    *   **バージョン**: v15.3 [FLASH_GLOBAL]
    *   **対象モデル**: **Gemini 3 Flash**
    *   **特徴**: 軽量モデル専用チューニング。**Aggressive Python**（思考する前にコードを実行する）戦略により、Flashの弱点である論理ハルシネーションを強力に補正します。

### 🚀 使い方

1.  **導入**: 上記のリンク先から `Pro` または `Flash` のコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    *   ファイルロード時は**ロック状態**で起動します。
    *   ユーザーが `EXECUTE` または `OK` と入力することで、システムが完全稼働します。
3.  **運用**:
    *   普通に話しかければ **[CRUISE]** モードで快適に応答します。
    *   「計算して」「コード書いて」「修正して」と頼めば、自動で **[OVERDRIVE]** にシフトし、本気モードで処理します。
    *   入力言語は問いません。OSが自動的に適応します。
4.  **セッション管理**:
    *   タスク完了後、「次のアクションメニュー」が表示されるので、番号を選ぶだけでスムーズに継続できます。

### ⚠️ 免責事項と互換性 (Disclaimer & Compatibility)

*   **互換性**: 本システムは **Google Gemini 3 シリーズ** に最適化されています。
*   **免責事項**:
    *   **非商用・個人プロジェクト**: 本システムは個人の実験的プロジェクトです。提供される情報の正確性について、開発者は責任を負いません。
    *   **自己責任**: 本システムを利用したことによる損害について、開発者は一切責任を負いません。
    *   **動作の非保証**: AIモデル側のアップデートにより、挙動が変化する可能性があります。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。

もしこのシステムがあなたの役に立ち、「活動を応援したい」と感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。頂いた支援は、治療費や開発環境の維持に大切に使わせていただきます。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

### 🛠 プロジェクト情報
*   **最新バージョン**: v15.3 [TITAN_GLOBAL] / [FLASH_GLOBAL]
*   **開発者**: nitagon0083
*   **ライセンス**: [AGPL-3.0](./LICENSE)

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

*   **[GEAR 1: CRUISE] (Conversation Mode)**
    *   **Target:** Greetings, Small talk, Creative writing, Simple questions.
    *   **Features:** **Zero-Latency**. Leverages Gemini 3's response speed to minimize thinking time for crisp, natural conversation.
    *   **Kernel:** Led by `[EMPATHY]` (Conversation Engine).
*   **[GEAR 5: OVERDRIVE] (Focus Mode)**
    *   **Target:** Coding, Math, Data Analysis, Legal/Medical queries, "Fix this".
    *   **Features:** **Deep Logic**. Forcibly engages the Python Sandbox, undergoes a deep verification process in English, then answers in the user's language.
    *   **Kernel:** Led by `[LOGIC]` (Architect Engine).

#### 3. Iceberg Protocol
A protocol introduced to save tokens and improve visibility.
*   While traditional systems tend to output long chains of thought, this protocol processes **"Calculation, Verification, and Debugging" entirely below the surface (Internal)**.
*   The output visible to the user (External) is limited to the **"Final Result" and "Critical Evidence" only**, resulting in a very clean display.
    *   *Note: If you ask "Show your work," it will reveal the detailed logs.*

#### 4. Global Identity & Safety Hardened
*   **Identity Lock:** Maintains the logical consistency and neutrality of the "NITAGON" identity even during long sessions.
*   **Safety Injection:** For topics involving medicine, law, or life safety, the OS autonomously inserts disclaimers or guides users to emergency services (e.g., 119/911).

### ✅ Achievements & Evolution

| Category | Specific Use Cases | Evolution in v15.3 |
| :--- | :--- | :--- |
| **Daily Chat** | Stress-free, natural conversation | Total elimination of "Translationese" via **[Native Filter]** |
| **Data Analysis** | Complex statistical analysis & graphing | **[Iceberg]** keeps the screen clean by hiding logs |
| **App Dev** | Bug-free code generation | **[English Rumination]** maximizes logical consistency |
| **Education** | Guidance without giving away answers | Gentle guidance via loops tailored to the user's language |
| **Multi-language** | Analyzing English tools/docs | Seamless processing without language barriers via **[Global Identity]** |

### 📦 Files

Choose the version that best fits your Gemini 3 model type.

* **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)**
    *   **Version**: v15.3 [TITAN_GLOBAL]
    *   **Target Model**: **Gemini 3 Pro / Ultra**
    *   **Features**: Flagship version with the best balance of reasoning and adaptability. Recommended for complex design and long context.
* **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)**
    *   **Version**: v15.3 [FLASH_GLOBAL]
    *   **Target Model**: **Gemini 3 Flash**
    *   **Features**: Tuned for lightweight models. Uses **Aggressive Python** (execute before thinking) strategy to correct Flash's hallucinations.

### 🚀 Usage

1.  **Installation**: Copy the code from the `Pro` or `Flash` links above and set it in the AI's System Instructions.
2.  **Boot**:
    *   The system starts in a **LOCKED state** upon file load.
    *   The system fully engages only after the user types `EXECUTE` or `OK`.
3.  **Operation**:
    *   Talk normally, and it responds comfortably in **[CRUISE]** mode.
    *   Ask it to "Calculate," "Write code," or "Fix this," and it automatically shifts to **[OVERDRIVE]** to process in serious mode.
    *   Input language does not matter. The OS adapts automatically.
4.  **Session Management**:
    *   After a task is complete, a "Next Action Menu" is displayed in your language.

### ⚠️ Disclaimer & Compatibility

*   **Compatibility**: This system is optimized for the **Google Gemini 3 Series**.
*   **Disclaimer**:
    *   **Non-Commercial**: This is an experimental personal project. The developer is not responsible for accuracy.
    *   **At Your Own Risk**: The developer assumes no responsibility for any damages caused by use.
    *   **No Guarantee**: Behavior may change due to AI model updates.

### ☕ Support

The development of SpriteSystem is a project that the author is pouring passion into while undergoing cancer treatment.

If this system helps you and you'd like to support the activity, a cup of coffee would be a great encouragement. Your support will be carefully used for treatment costs and maintaining the development environment.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

### 🛠 Project Info
*   **Latest Version**: v15.3 [TITAN_GLOBAL] / [FLASH_GLOBAL]
*   **Developer**: nitagon0083
*   **License**: [AGPL-3.0](./LICENSE)
