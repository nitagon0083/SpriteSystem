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

## 💎 実証：Flash版による「シニア級エンジニアリング」の完遂

「軽量モデルであるFlashは、複雑な設計には向かない」という常識は、SpriteSystemによって覆されました。以下は、**Gemini 3 Flash (v15.5.1)** を使用し、本OSの制御下で生成された実際の成果物（Evidence）です。

### **【Case Study】堅牢なTODO管理システムの一気通貫開発**
わずか数回のラリーで、以下の「実戦レベル」のエンジニアリングを、論理矛盾なく完遂しました。

#### **1. Database Architecture (Prisma)**
- **Optimistic Locking**: 複数端末からの同時更新を防ぐ `version` カラムを用いた排他制御を自発的に実装。
- **Referential Integrity**: ユーザー削除時に紐づくデータを自動削除する `onDelete: Cascade` の設定。
- **Performance**: 頻出クエリを予見した `@@index([userId, status])` などの複合インデックス設計。



#### **2. Service Layer & Validation (TypeScript)**
- **Atomic Transactions**: `Prisma.$transaction` を用い、データの整合性を物理的に保証。
- **Strict Validation**: **Zod** を使用し、API境界で「未来の日付チェック」や「型変換」を厳格に実行。

#### **3. Automated Testing (Jest)**
- **Edge Case Testing**: 正常系だけでなく、「バージョンの不一致」や「権限侵害」といった異常系を網羅したテストコードを生成。
- **Mock Strategy**: `prismaMock` を活用した、高速かつ正確な論理検証。

#### **4. CI/CD Pipeline (GitHub Actions)**
- **Quality Gate**: プッシュ時に自動でテスト・ビルド・カバレッジ確認を行うワークフローを定義。



---

### **📈 なぜ「どこの馬の骨かもわからない素人」がこれを作れたのか？**

その答えは、SpriteSystemが持つ **「論理の檻（Logic Cage）」** にあります。

1.  **情報の非破壊性 (ZERO_LOSS)**:
    AIが勝手にコードを省略したり、重要な制約を忘れることをプロトコルレベルで禁止。
2.  **思考の深度化 (INTERNAL: English)**:
    日本語の曖昧さに逃げず、モデル内部で一度英語論理に変換して思考させることで、シニアエンジニア並みの深い洞察を引き出します。
3.  **役割の強制 (OS Kernel)**:
    AIを「チャットボット」ではなく「高密度演算エンジン」として初期化するため、謝罪や無駄な挨拶を排除し、100%のリソースをエンジニアリングに集中。

> **「このシステムがあれば、ジュニアエンジニアでも、無料版AIで、シニア級のアウトプットを安定して出せるようになる。」**
> これこそが、SpriteSystemが提供する真の価値です。

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
| **[SpriteSystem_Flash_JP.md](./OS/JP/SpriteSystem_Flash_JP.md)** | **v15.5.1 [FLASH_EVOLUTION]** | **Gemini 3 Flash** | **【高速・演算】**<br>XML記述による軽量化。ミスを許さない高速処理向け。 |

#### 🇺🇸 英語版 (English Editions)
*思考から出力まで完全英語。最も論理ロスが少ない構成です。*

| File | Version | Best For | Features |
| :--- | :--- | :--- | :--- |
| **[SpriteSystem_Pro_EN.md](./OS/EN/SpriteSystem_Pro_EN.md)** | **v15.5 [TITAN_EVOLUTION_EN]** | **Gemini 3 Pro** | **[Partner / Architect]**<br>Includes Preview & Anchoring for complex workflows. |
| **[SpriteSystem_Flash_EN.md](./OS/EN/SpriteSystem_Flash_EN.md)** | **v15.5.1 [FLASH_EVOLUTION_EN]** | **Gemini 3 Flash** | **[Machine / Engineer]**<br>XML-based instruction for maximum speed & adherence. |

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

---

## 💎 Evidence: Achieving Senior-Level Engineering with Gemini 3 Flash

The common belief that "lightweight models like Flash are unsuitable for complex design" has been debunked by SpriteSystem. Below are the actual engineering results achieved with **Gemini 3 Flash (v15.5.1)** under this OS control.

### **【Case Study】End-to-End Development of a Robust TODO System**
In just a few turns, the following production-ready engineering tasks were completed with perfect logical consistency:

#### **1. Database Architecture (Prisma)**
- **Optimistic Locking**: Implemented concurrency control using a `version` column to prevent data corruption from simultaneous updates.
- **Referential Integrity**: Configured `onDelete: Cascade` to ensure no orphaned records.
- **Performance Optimization**: Designed composite indexes such as `@@index([userId, status])` predicting high-frequency query patterns.



#### **2. Service Layer & Validation (TypeScript)**
- **Atomic Transactions**: Utilized `Prisma.$transaction` to physically guarantee data integrity.
- **Strict Validation**: Leveraged **Zod** to enforce strict API boundary checks, including future-date validation and type coercion.

#### **3. Automated Testing (Jest)**
- **Edge Case Coverage**: Generated comprehensive tests for failure modes, including "version mismatch" and "unauthorized access."
- **Mocking Strategy**: Applied a sophisticated `prismaMock` approach for fast and accurate logic verification.

#### **4. CI/CD Pipeline (GitHub Actions)**
- **Quality Gatekeeping**: Defined a workflow to automate testing, building, and coverage reporting upon every push.

---

### **📈 Why can an "unknown" system achieve this?**

The secret lies in the **"Logic Cage"** architecture of SpriteSystem:

1.  **ZERO_LOSS Protocol**:
    Prohibits the AI from omitting code or forgetting critical constraints at the protocol level.
2.  **INTERNAL: English Inference**:
    Bypasses the ambiguity of natural language by forcing the model to think in logical English structures, extracting senior-level insights.
3.  **Kernel Initialization**:
    Initializes the AI as a "High-Density Logic Engine" rather than a "Chatbot," dedicating 100% of resources to engineering by eliminating unnecessary conversational overhead.

> **"This system empowers junior developers to consistently produce senior-level output using free-tier AI models."**
> This is the true power and mission of SpriteSystem.
### 📦 Select Your Edition

| Edition | Version | Language | Target Model |
| :--- | :--- | :--- | :--- |
| **Pro JP** | v15.5 [TITAN_EVOLUTION] | Japanese | Gemini 3 Pro |
| **Flash JP** | v15.5.1 [FLASH_EVOLUTION] | Japanese | Gemini 3 Flash |
| **Pro EN** | v15.5 [TITAN_EVOLUTION_EN] | English | Gemini 3 Pro |
| **Flash EN** | v15.5.1 [FLASH_EVOLUTION_EN] | English | Gemini 3 Flash |

### 🚀 Usage
1.  Copy the code for your desired edition.
2.  Paste into System Instructions.
3.  **Pro:** Type `EXECUTE` to unlock. **Flash:** Ready immediately.

*(See Japanese section for Support & Disclaimer)*
