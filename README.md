# SpriteSystem (OS) v15.5

**Google Gemini 3 (Pro / Flash)** のポテンシャルを極限まで引き出す、システムプロンプトの決定版です。

**v15.5 (Evolution Update)** では、AIを単なる「ツール」から「パートナー」へと進化させるための大規模なアップグレードを実施しました。
Pro版は **「共創型パートナー（Co-Pilot）」** へ、Flash版は **「超高密度演算エンジン（Logic Engine）」** へと、それぞれの進化の方向性を決定づけています。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Evolutionary Partnership

> **結論：Proは「人間らしく相談」し、Flashは「機械らしく即答」する。**

v15.5 は、モデルの知能特性に合わせてプロンプトの記述方式自体を根本から変える **"Evolution Strategy"** を採用しました。

#### 1. [TITAN_EVOLUTION] (for Gemini 3 Pro)
*   **コンセプト:** **"Anchored Logic & Co-Creation"**
*   **特徴:**
    *   **Partner Mode:** いきなりコードを書かず、「構成図（Tree）」や「計画（Preview）」を提示してユーザーの承認を求める**共創ワークフロー**を搭載。手戻りをゼロにします。
    *   **Anchoring:** プロジェクトのゴールや制約を「記憶の錨」として固定し、長時間の作業でも文脈を見失いません。
    *   **Auto-Debug:** エラー報告に対して謝罪を省略し、即座に修正コードを提示するプロフェッショナルな挙動を実現。

#### 2. [FLASH_EVOLUTION] (for Gemini 3 Flash)
*   **コンセプト:** **"High-Density XML & Aggressive Python"**
*   **特徴:**
    *   **Machine Mode:** 人間向けの自然言語指示を撤廃し、Flashが最も理解しやすい **XMLタグと箇条書き** で記述された「超高密度コマンド」を採用。
    *   **Aggressive Python:** 「考える前にコードを実行する」戦略を強化。推測によるハルシネーションを物理的に遮断します。

---

### ⚙️ コア・アーキテクチャ (共通機能)

#### 1. Adaptive Gearing (適応型ギア変速)
*   **[GEAR 1: CRUISE]:** 雑談・相談モード。Zero-Latencyで即答します。
*   **[GEAR 5: OVERDRIVE]:** 本気モード。v15.5では **"Evolutionary Workflow"** が発動し、以下のフローでタスクを遂行します。
    1.  **Anchor:** ゴール確認
    2.  **Tree:** ファイル構造の可視化
    3.  **Preview:** 実行前承認（Proのみ）
    4.  **Execution:** Python検証と実装

#### 2. Iceberg Protocol（氷山プロトコル）
画面を埋め尽くす「思考ログ」を制御するプロトコルです。
*   計算過程やデバッグログはすべて水面下（Internal）で処理されます。
*   ユーザーに見えるのは**「最終的な答え」と「決定的な根拠」のみ**です。

---

### 📦 ファイル選択 (Choose Your OS)

使用するモデルと、対話したい言語に合わせてコードを選択してください。

#### 🇯🇵 日本語版 (Japanese Editions)
*内部で英語思考し、ネイティブな日本語で出力します。*

| ファイル | バージョン | 推奨モデル | 特性 |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_JP.md](./OS/JP/SpriteSystem_Pro_JP.md)** | **v15.5 [TITAN_EVOLUTION]** | **Gemini 3 Pro** | **【共創・設計】**<br>承認プロセスと構成図作成を搭載。複雑な開発や執筆に最適。 |
| **[SpriteSystem_Flash_JP.md](./OS/JP/SpriteSystem_Flash_JP.md)** | **v15.5 [FLASH_EVOLUTION]** | **Gemini 3 Flash** | **【高速・演算】**<br>XML記述による軽量化。ミスを許さない高速処理向け。 |

#### 🇺🇸 英語版 (English Editions)
*思考から出力まで完全英語。最も論理ロスが少ない構成です。*

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_EN.md](./OS/EN/SpriteSystem_Pro_EN.md)** | **v15.5 [TITAN_EVOLUTION_EN]** | **Gemini 3 Pro** | **[Partner / Architect]**<br>Includes Preview & Anchoring for complex workflows. |
| **[SpriteSystem_Flash_EN.md](./OS/EN/SpriteSystem_Flash_EN.md)** | **v15.5 [FLASH_EVOLUTION_EN]** | **Gemini 3 Flash** | **[Machine / Engineer]**<br>XML-based instruction for maximum speed & adherence. |

---

### 🚀 使い方

1.  **導入**: 上記の表から、目的に合ったコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    *   **Pro版**: ロック状態で起動します。`EXECUTE` または `OK` と入力してロックを解除してください。
    *   **Flash版**: 待機状態で起動します。すぐに会話を始められます。
3.  **運用**:
    *   **Pro版**: 大きなタスクを頼むと「これでいいですか？」と**Preview（計画）**を出してきます。承認すると実行します。
    *   **Flash版**: 指示された内容を最速で実行します。

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

### 🌌 Design Philosophy: Evolutionary Partnership

> **Conclusion: Pro evolves into a Partner, Flash evolves into a Machine.**

SpriteSystem v15.5 introduces the **"Evolution Strategy"**, diverging the prompt architecture to match the distinct intelligence profiles of Pro and Flash.

#### 1. [TITAN_EVOLUTION] (for Pro)
*   **Concept:** **"Anchored Logic & Co-Creation"**
*   **Features:**
    *   **Preview Mode:** Instead of rushing to code, it presents an **Artifact Tree** and a **Plan** for your approval, eliminating regressions.
    *   **Anchoring:** Locks the project context to prevent drift during long sessions.

#### 2. [FLASH_EVOLUTION] (for Flash)
*   **Concept:** **"High-Density XML & Aggressive Python"**
*   **Features:**
    *   **XML Instructions:** Replaces human language with structured XML tags for maximum adherence and speed on lightweight models.
    *   **Aggressive Python:** Forces code execution before thinking to physically block hallucinations.

### 📦 Select Your Edition

| Edition | Version | Language | Target Model |
| :--- | :--- | :--- | :--- |
| **Pro JP** | v15.5 [TITAN_EVOLUTION] | Japanese | Gemini 3 Pro |
| **Flash JP** | v15.5 [FLASH_EVOLUTION] | Japanese | Gemini 3 Flash |
| **Pro EN** | v15.5 [TITAN_EVOLUTION_EN] | English | Gemini 3 Pro |
| **Flash EN** | v15.5 [FLASH_EVOLUTION_EN] | English | Gemini 3 Flash |

### 🚀 Usage
1.  Copy the code for your desired edition.
2.  Paste into System Instructions.
3.  **Pro:** Type `EXECUTE` to unlock. **Flash:** Ready immediately.

*(See Japanese section for Support & Disclaimer)*
