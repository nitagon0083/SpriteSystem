# SpriteSystem (OS) v15.2.1

**Google Gemini 3 (Pro / Flash)** のポテンシャルを極限まで引き出す、システムプロンプトの決定版です。

実験的な **v15.3 (Global Dynamic)** での運用結果（汎用化による論理精度の希釈）を踏まえ、本プロジェクトは **最も評価の高かった v15.2 ベース** へと回帰しました。
さらに、**「モデル（Pro/Flash）」**と**「言語（Japanese/English）」**のそれぞれに完全に特化したカーネルを用意する **"Quad-Edition Strategy"** を採用しました。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Quad-Core Optimization

> **結論：万能なプロンプトは捨てた。モデルと言語に合わせた「専用OS」こそが最強である。**

v15.2.1 は、動的な言語検知プロセスを排除し、**「あらかじめターゲット言語に固定されたOS」**を使用することで、余計なオーバーヘッドをゼロにしました。

#### 1. Model Optimization (モデル別最適化)
*   **[TITAN] (for Gemini 3 Pro):**
    *   **"Deep Logic & Strict Control"**。Proの高い推論能力を活かし、長文の英語思考（Rumination）と厳格なSearch/Replaceを強制します。IDE連携や複雑な設計に最適です。
*   **[FLASH] (for Gemini 3 Flash):**
    *   **"Speed & Aggressive Python"**。Flashの弱点（論理ハルシネーション・フリーズ）を、箇条書き思考と「即コード実行」戦略で物理的にカバーした外科的チューニング版です。

#### 2. Language Optimization (言語別最適化)
*   **Japanese Edition:** 内部は英語で思考し、出力時に**「翻訳調を排除した自然な日本語」**へ変換します。
*   **English Edition:** 内部思考から出力まで**完全な英語**で統一。翻訳レイヤーが存在しないため、論理純度と応答速度が最も高くなります。

---

### ⚙️ コア・アーキテクチャ (共通機能)

全エディションに以下の強力な機能（Adaptive Gearing）を搭載しています。

#### 1. Adaptive Gearing (自動変速)
タスクの密度に応じて、OSが自動的に処理モードを切り替えます。
*   **[GEAR 1: CRUISE]:** 雑談・相談モード。思考時間を最小化し、Zero-Latencyで応答。
*   **[GEAR 5: OVERDRIVE]:** 本気モード。数学・コード・分析時は、必ず裏側でPython検証を行ってから回答します。

#### 2. Iceberg Protocol（氷山プロトコル）
画面を埋め尽くす「思考ログ」を制御するプロトコルです。
*   ユーザーに見えるのは**「最終的な答え」と「決定的な根拠」のみ**です。
*   計算過程やデバッグログはすべて水面下（Internal）で処理されます。

---

### 📦 ファイル選択 (Choose Your OS)

使用するモデルと、対話したい言語に合わせてコードを選択してください。

#### 🇯🇵 日本語版 (Japanese Editions)
*内部で英語思考し、ネイティブな日本語で出力します。*

| ファイル | バージョン | 推奨モデル | 特性 |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_JP.md](./OS/JP/Pro.md)** | **v15.2.1 [TITAN_REFINED]** | **Gemini 3 Pro** | **【最高精度・厳格】**<br>開発・設計・執筆向け。エディタ連携強化版。 |
| **[SpriteSystem_Flash_JP.md](./OS/JP/Flash.md)** | **v15.2.1 [FLASH_REFINED]** | **Gemini 3 Flash** | **【高速・安定】**<br>計算ミス防止機能搭載。日常・学習・チャット向け。 |

#### 🇺🇸 英語版 (English Editions)
*思考から出力まで完全英語。最も論理ロスが少ない構成です。*

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_EN.md](./OS/EN/Pro.md)** | **v15.2.1 [TITAN_REFINED_EN]** | **Gemini 3 Pro** | **[Logic Pure]**<br>No translation layer. Maximum reasoning density. |
| **[SpriteSystem_Flash_EN.md](./OS/EN/Flash.md)** | **v15.2.1 [FLASH_REFINED_EN]** | **Gemini 3 Flash** | **[Speed Pure]**<br>Optimized for stability and instant response. |

---

### 🚀 使い方

1.  **導入**: 上記の表から、目的に合ったコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    *   **Pro版**: ロック状態で起動します。`EXECUTE` または `OK` と入力してロックを解除してください。
    *   **Flash版**: 待機状態で起動します。すぐに会話を始められます。
3.  **運用**:
    *   普段は **[CRUISE]** モードで快適に応答します。
    *   「計算して」「コード書いて」と頼めば、自動で **[OVERDRIVE]** にシフトします。

### ⚠️ 免責事項 (Disclaimer)

*   **互換性**: 本システムは **Google Gemini 3 シリーズ** に最適化されています。
*   **免責**: 本システムは個人の実験的プロジェクトです。出力の正確性や、利用による損害について開発者は責任を負いません。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。
もしこのシステムがあなたの役に立ち、活動を応援したいと感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)

---
---

## 🇺🇸 English (Summary)

### 🌌 Design Philosophy: Quad-Core Optimization

> **Conclusion: Logic purity over versatility.**

SpriteSystem v15.2.1 abandons the "Global Dynamic" approach of v15.3 in favor of **static, specialized kernels**. We now offer four distinct editions optimized for specific Model/Language combinations.

#### 1. Model Optimization
*   **[TITAN] (Pro):** Focuses on deep English rumination and strict coding controls (Search/Replace).
*   **[FLASH] (Flash):** Focuses on "Aggressive Python" (execute before thinking) to prevent hallucinations.

#### 2. Language Optimization
*   **Japanese Editions:** Think in English, output in **Native Natural Japanese**.
*   **English Editions:** Think in English, output in **Professional English**. (Zero translation overhead).

### 📦 Select Your Edition

| Edition | Version | Language | Target Model |
| :--- | :--- | :--- | :--- |
| **Pro JP** | v15.2.1 [TITAN_REFINED] | Japanese | Gemini 3 Pro |
| **Flash JP** | v15.2.1 [FLASH_REFINED] | Japanese | Gemini 3 Flash |
| **Pro EN** | v15.2.1 [TITAN_REFINED_EN] | English | Gemini 3 Pro |
| **Flash EN** | v15.2.1 [FLASH_REFINED_EN] | English | Gemini 3 Flash |

### 🚀 Usage
1.  Copy the code for your desired edition.
2.  Paste into System Instructions.
3.  **Pro:** Type `EXECUTE` to unlock. **Flash:** Ready immediately.

*(See Japanese section for Support & Disclaimer)*
