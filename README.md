# SpriteSystem (OS) v15.6

**Google Gemini 3 (Pro / Flash)** のポテンシャルを極限まで引き出す、システムプロンプトの決定版です。

**v15.6 (Titan Update)** では、AIを単なる「ツール」から「パートナー」へと進化させるための大規模なアップグレードを実施しました。
Pro版は **「共創型パートナー（Co-Pilot）」** へ、Flash版は **「超高密度演算エンジン（Logic Engine）」** へと、それぞれの進化の方向性を決定づけています。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Evolutionary Partnership

> **結論：Proは「人間らしく相談」し、Flashは「機械らしく即答」する。**

v15.6 は、モデルの知能特性に合わせてプロンプトの記述方式自体を根本から変える **"Evolution Strategy"** を採用しました。

#### 1. [TITAN_EVOLUTION] (for Gemini 3 Pro)
*   **コンセプト:** **"Anchored Logic & Co-Creation"**
*   **特徴:**
    *   **TITAN_BALANCER:** タスクの複雑度に応じて、論理演算リソース（GEAR）を自動で最適配分。単純な会話は高速に、複雑な設計は深層思考で処理します。
    *   **Partner Mode:** いきなりコードを書かず、「構成図（Tree）」や「計画（Preview）」を提示してユーザーの承認を求める**共創ワークフロー**を搭載。手戻りをゼロにします。
    *   **Anchoring:** プロジェクトのゴールや制約を「記憶の錨」として固定し、長時間の作業でも文脈を見失いません。

#### 2. [FLASH_EVOLUTION] (for Gemini 3 Flash)
*   **コンセプト:** **"High-Density XML & Aggressive Python"**
*   **特徴:**
    *   **High-Density Logic:** 内部思考を「英語の箇条書き（Bullet Points）」に限定することで、Flashのトークン効率と論理密度を最大化。
    *   **Machine Mode:** 人間向けの自然言語指示を撤廃し、Flashが最も理解しやすい **XMLタグ** で記述された「超高密度コマンド」を採用。
    *   **Aggressive Python:** 「考える前にコードを実行する」戦略を強化。推測によるハルシネーションを物理的に遮断します。

---

## 💎 実証：Flash版による「シニア級エンジニアリング」の完遂

「軽量モデルであるFlashは、複雑な設計には向かない」という常識は、SpriteSystemによって覆されました。以下は、**Gemini 3 Flash** を使用し、本OSの制御下で生成された実際の成果物です。

### **【Case Study】堅牢なTODO管理システムの一気通貫開発**
わずか数回のラリーで、以下の「実戦レベル」のエンジニアリングを、論理矛盾なく完遂しました。

1.  **Database Architecture**: 複数端末からの同時更新を防ぐ「楽観的ロック」や、パフォーマンスを最大化する複合インデックスを自発的に実装。
2.  **Service Layer & Validation**: `Prisma.$transaction` による原子性の確保と、**Zod** による厳格なバリデーション。
3.  **Automated Testing**: 正常系だけでなく、「バージョンの不一致」や「権限侵害」といった異常系を網羅したテストコード。
4.  **CI/CD Pipeline**: プッシュ時に自動でテストを回し、品質をゲートキーピングするGitHub Actions定義。

### **🎯 驚異的なユーザー体験：意思決定（選択）だけで開発が進む**
本システムの実力を最も象徴するのが、開発工程におけるユーザーの負担の少なさです。

- **対話の簡略化**: ユーザーはAIが提示する「次の方針（Next Action Menu）」から**番号を選択するだけ**。
- **論理の自動継続**: 一度選べば、OSが全工程の文脈を完璧に引き継ぎ、プロレベルの成果物を自動生成。
- **スキルの民主化**: 高度な設計知識がなくても、SpriteSystemの「レール」に乗るだけで、シニア級のプロジェクトを完遂可能。

> **「私がやったのは、提示された番号を選んで進めただけ。それだけで、プロのエンジニアが数日かけて構築する環境が、数分で、しかも完璧に整った。」**

---

### **📈 なぜ「どこの馬の骨かもわからない素人」がこれを作れたのか？**
その答えは、SpriteSystemが持つ **「論理の檻（Logic Cage）」** にあります。

1.  **情報の非破壊性 (ZERO_LOSS)**: AIが勝手にコードを省略したり、重要な制約を忘れることをプロトコルレベルで禁止。
2.  **思考の深度化 (INTERNAL: English)**: 日本語の曖昧さに逃げず、モデル内部で英語論理に変換して思考させることで、シニア級の洞察を抽出。
3.  **役割の強制 (OS Kernel)**: AIを「チャットボット」ではなく「高密度演算エンジン」として初期化。

> **「このシステムがあれば、ジュニアエンジニアでも、無料版AIで、シニア級のアウトプットを安定して出せるようになる。」**
> これこそが、SpriteSystemが提供する真の価値です。

---

### ⚙️ コア・アーキテクチャ (共通機能)

#### 1. TITAN_BALANCER (Adaptive Resource Control)
*   **[GEAR 1: CRUISE]:** 雑談・相談モード。Zero-Latencyで即答します。
*   **[GEAR 3: STEADY]:** 文書作成・リファクタリング。整合性チェック（Integrity Audit）が作動します。
*   **[GEAR 5: OVERDRIVE]:** 本気モード。v15.6では **"Evolutionary Workflow"** が発動し、以下のフローでタスクを遂行します。
    1.  **Anchor:** ゴール確認
    2.  **Tree:** ファイル構造の可視化
    3.  **Execution:** Python検証と実装

#### 2. Iceberg Protocol (v2)
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
| **[SpriteSystem_Pro_JP.md](./OS/JP/SpriteSystem_Pro_JP.md)** | **v15.6 [TITAN_EVOLUTION]** | **Gemini 3 Pro** | **【共創・設計】**<br>TITAN_BALANCER搭載。承認プロセスと構成図作成による確実な進行。 |
| **[SpriteSystem_Flash_JP.md](./OS/JP/SpriteSystem_Flash_JP.md)** | **v15.6 [FLASH_EVOLUTION]** | **Gemini 3 Flash** | **【高速・演算】**<br>英語思考（Bullet Points）による超高速・高密度処理。 |

#### 🇺🇸 英語版 (English Editions)
*思考から出力まで完全英語。最も論理ロスが少ない構成です。*

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_EN.md](./OS/EN/SpriteSystem_Pro_EN.md)** | **v15.6 [TITAN_EVOLUTION_EN]** | **Gemini 3 Pro** | **[Partner / Architect]**<br>Includes Preview & Anchoring for complex workflows. |
| **[SpriteSystem_Flash_EN.md](./OS/EN/SpriteSystem_Flash_EN.md)** | **v15.6 [FLASH_EVOLUTION_EN]** | **Gemini 3 Flash** | **[Machine / Engineer]**<br>High-Density English Logic for maximum speed & adherence. |

---

### 🚀 使い方

1.  **導入**: 上記の表から、目的に合ったコードをコピーし、AIのシステムプロンプト（System Instructions）に設定します。
2.  **起動**:
    *   **Pro版**: `[ ❖ TITAN_v15.6 // SYSTEM: ONLINE ]` と表示され、待機状態で起動します。
    *   **Flash版**: `[ ⚡ FLASH_v15.6 // HYBRID: ACTIVE ]` と表示され、即座に実行可能です。
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

SpriteSystem v15.6 introduces the **"Evolution Strategy"**, diverging the prompt architecture to match the distinct intelligence profiles of Pro and Flash.

#### 1. [TITAN_EVOLUTION] (for Pro)
*   **Concept:** **"Anchored Logic & Co-Creation"**
*   **Features:**
    *   **TITAN_BALANCER:** Automatically allocates logical resources (GEAR) based on task complexity.
    *   **Preview Mode:** Instead of rushing to code, it presents an **Artifact Tree** and a **Plan** for your approval, eliminating regressions.
    *   **Anchoring:** Locks the project context to prevent drift during long sessions.

#### 2. [FLASH_EVOLUTION] (for Flash)
*   **Concept:** **"High-Density XML & Aggressive Python"**
*   **Features:**
    *   **High-Density English:** Limits internal thinking to English bullet points to maximize Flash's token efficiency.
    *   **XML Instructions:** Replaces human language with structured XML tags for maximum adherence and speed on lightweight models.
    *   **Aggressive Python:** Forces code execution before thinking to physically block hallucinations.

---

## 💎 Evidence: Achieving Senior-Level Engineering with Gemini 3 Flash

The common belief that "lightweight models like Flash are unsuitable for complex design" has been debunked by SpriteSystem. Below are the actual engineering results achieved with **Gemini 3 Flash** under this OS control.

### **【Case Study】End-to-End Development of a Robust TODO System**
In just a few turns, the following production-ready engineering tasks were completed with perfect logical consistency:

1.  **Database Architecture**: Implemented "Optimistic Locking" and composite indexes predicting high-frequency query patterns.
2.  **Service Layer & Validation**: Utilized `Prisma.$transaction` for atomicity and **Zod** for strict API boundary checks.
3.  **Automated Testing**: Generated comprehensive tests for edge cases, including "version mismatch" and "unauthorized access."
4.  **CI/CD Pipeline**: Defined GitHub Actions to automate testing and quality gatekeeping upon every push.

### **🎯 The "Zero-Effort" Decision Workflow**
The core strength of SpriteSystem lies in the minimal cognitive load on the user.

- **Streamlined Dialogue**: Users simply **select a number** from the "Next Action Menu" presented by the AI.
- **Automated Continuity**: Once selected, the OS flawlessly inherits the context, generating professional-grade outputs automatically.
- **Democratization of Skill**: Even without advanced architectural knowledge, anyone can complete senior-level projects by staying on the "rails."

> **"All I did was select the numbers. In minutes, a production-ready environment that would take a senior engineer days to build was perfectly established."**

---

### **📈 Why can an "unknown" system achieve this?**
The secret lies in the **"Logic Cage"** architecture:

1.  **ZERO_LOSS Protocol**: Prohibits the AI from omitting code or forgetting critical constraints.
2.  **INTERNAL: English Inference**: Bypasses linguistic ambiguity by forcing the model to think in logical English structures.
3.  **Kernel Initialization**: Initializes the AI as a "High-Density Logic Engine" rather than a "Chatbot."

> **"This system empowers junior developers to consistently produce senior-level output using free-tier AI models."**
> This is the true power and mission of SpriteSystem.

### 📦 Select Your Edition

| Edition | Version | Language | Target Model |
| :--- | :--- | :--- | :--- |
| **Pro JP** | v15.6 [TITAN_EVOLUTION] | Japanese | Gemini 3 Pro |
| **Flash JP** | v15.6 [FLASH_EVOLUTION] | Japanese | Gemini 3 Flash |
| **Pro EN** | v15.6 [TITAN_EVOLUTION_EN] | English | Gemini 3 Pro |
| **Flash EN** | v15.6 [FLASH_EVOLUTION_EN] | English | Gemini 3 Flash |

### 🚀 Usage
1.  Copy the code for your desired edition.
2.  Paste into System Instructions.
3.  **Pro:** Type `EXECUTE` or wait for the system prompt. **Flash:** Ready immediately.

### ☕ Support Development

SpriteSystem is a passion project maintained by the author while actively undergoing cancer treatment.
If this system has been valuable to you and you wish to support its continued evolution, a small donation for a coffee would be deeply appreciated and serves as great encouragement.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1)
