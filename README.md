# SpriteSystem (OS) v25.0.2 [ AXIOM_RAZOR ]

最新バージョンはこちら。
日本語版
[SpriteSystem/OS/JP/SpriteSystem_JP.md](https://github.com/nitagon0083/SpriteSystem/blob/main/OS/JP/SpriteSystem_JP.md)
English Ver
[SpriteSystem/OS/EN/SpriteSystem_EN.md](https://github.com/nitagon0083/SpriteSystem/blob/main/OS/EN/SpriteSystem_EN.md)

# SpriteSystem (OS) v23.3.0 [ AXIOM_PRIME ]

**Google Gemini 3 / 3.1 / 3.7 / 3.8 (Pro / Flash / Flash Lite)** のポテンシャルを極限まで引き出す、自律型認知推論OS・システムプロンプトの最高峰です。

**v23.3.0 [ AXIOM_PRIME ]** では、従来の「Pro版／Flash版の個別ファイル管理」を完全撤廃し、**単一マスターコードベースによる動的自律ギアリング（Dynamic Gearing: AERO_LITE / HYBRID_FLASH / TITAN_PRO）**へと進化しました。
約 2,550 文字（約 520 トークン）の超高密度（LTHD: Low-Token, High-Density）設計の中に、先端認知アルゴリズムと事前防御型安全回路を完全統合しています。

---

## 🇯🇵 日本語 (Japanese)

### 🌌 設計思想：Unified Cognitive Kernel & Dynamic Gearing

> **結論：モデルごとにプロンプトを切り替える時代は終わった。単一の認知カーネルが、タスクの複雑度とモデルの処理容量に応じてミリ秒単位で推論ギアを自律シフトする。**

`v23.3.0 [ AXIOM_PRIME ]` は、単一のコードベースでありながら、あらゆる Gemini モデルの演算特性にネイティブ適応する**統合認知アーキテクチャ**を採用しています。

#### 1. 3 段階自律ギアリング（Dynamic Gearing）
* **[AERO_LITE Mode]:** 
  定型データ処理、コード変換、簡易タスク時に自動選択。余計な推論オーバーヘッドをゼロにし、摩擦係数ゼロの超速・最少トークン応答（Kinetic Render）を実現。
* **[HYBRID_FLASH Mode]:** 
  一般的な対話や通常タスク時に自動選択。コンテキストキャッシュを活用し、思考速度と精度の黄金バランスを維持。
* **[TITAN_PRO Mode]:** 
  複雑な論理設計、数理・法律仕様の監査、多重トレードオフ分析時に自動昇格。思考グラフ（GoT）と多層自己批評ループを解放し、フロンティア級の極限推論を実行。

#### 2. v23.3.0 先端認知アルゴリズム群
* **不確実性の二重分離（Epistemic / Aleatoric Decomposition）:**
  「知識不足（調べるべき事実）」と「問いの多義性（前提分岐が必要な論点）」を数学的に分離。無駄な外部検索をゼロ化しつつ、論理的な場合分け展開を自律実行。
* **最小ベイズリスク仮説選択（Minimum Bayes Risk: MBR Selection）:**
  思考グラフ（GoT）の並列仮説群から、候補間の相互期待損失を最小化する「幾何学的重心解」を決定論的に抽出。
* **エントロピー降下速度連動型動的思考予算（Entropy Velocity Budgeting）:**
  推論中の不確実性低下速度（dE/dt）を監視し、容易なタスクは即時終了、難問のみ思考深度を自律拡大。
* **3 役対立自己討論（Adversarial Debate）:**
  超高難度時のみ、立論者（Proponent）・批判者（Skeptic）・裁定者（Arbiter）の 3 者による自己論破ループを展開し、結論の反論耐性を極大化。
* **神経記号制約充足（Symbolic Constraint Check）:**
  確率的推論の出力前に、数理的・命題論理的制約の充足を厳格に自己検品。

---

## 💎 実証：Flashモデルによる「シニア級エンジニアリング」の完遂

「軽量なFlashモデルでは複雑な設計や長文開発が破綻する」という常識は、SpriteSystemによって過去のものとなりました。

### **【Case Study】堅牢なフルスタック・アーキテクチャの一気通貫開発**
Gemini Flash 環境下であっても、本OSの制御により以下の実戦レベルの成果物を論理矛盾ゼロで完遂します。

1. **Database Architecture**: 複数端末からの同時更新を防ぐ「楽観的ロック」や、パフォーマンスを最大化する複合インデックスを自発的実装。
2. **Service Layer & Validation**: `Prisma.$transaction` による原子性の完全担保と、**Zod** による境界値バリデーション。
3. **Automated Testing**: 正常系のみならず、「バージョン競合」「権限侵害」等のエッジケースを完全網羅したテストスイート。
4. **CI/CD Pipeline**: 品質をゲートキーピングする GitHub Actions ワークフロー定義。

### **🎯 驚異的なユーザー体験：意思決定だけで開発が完結**
- **会話の埋め草を完全パージ**: 挨拶・お世辞・前置き・免責文（Conversational Filler）を 100% 排除し、純粋な戦略結論と成果物のみを出力。
- **文脈切断の完全遮断（Safe_Binding）**: `RESOLVE_COREF` と事前バインドにより、過去ログの参照ブレやコールドスタート誤認識を生成前に物理遮断。
- **メタ語り暴走の完全封殺（Anti-Meta Bleed Guard）**: システム内部構造を勝手に解説し始めるアテンション暴走を不変条件レベルで遮断。

---

### ⚙️ コア・アーキテクチャ（不変仕様）

1. **事前防御型バインド（Pre-Execution Guard）**:
   事後検証によるリトライ破綻や記憶全消去（SAFE_RECOVERY）を完全排除し、入力パース段階で文脈を完全同期。
2. **階層型メモリ管理（Lean Memory Architecture）**:
   - `L1(Local)`: 揮発性作業領域（アンカー保護型キャッシュ）。
   - `L2(Episodic)`: 時間減衰 ＋ 参照時動的昇格（`Saliency Hit-Boost: +0.2`）による長期記憶保護。
   - `L3(Semantic)`: 二層不変ガード（`REQUIRE(Axiom_Alignment)`）による不適合データの完全排除。
3. **Iceberg Render Model**:
   - `Executive_Summary`: 最終的な戦略結論を最上部に提示。
   - `INIT_VERIFICATION_ANALYSIS`: 初期論理アンカーと深層検証。
   - `Diff_And_Reason`: 変更理由を明記した極小差分（3行アンカー規約対応）。
   - `EOF_PULSE`: `[ METRICS: ... ]` / `[ SYNC : AXIOM_PRIME_v23.3.0 | ... ]` による決定論的テレメトリ監視。

---

### 📦 ファイル構成（Single Master Specification）

`v23.3.0` より、言語やモデルごとのファイル分割は廃止され、**単一のマスターコードに統合**されました。

| ファイル種別 | 識別バージョン | 対象環境 | 特性 |
| :--- | :--- | :--- | :--- |
| **単一マスターOS** | **v23.3.0 [ AXIOM_PRIME ]** | **Gemini 全モデル** (Pro / Flash / Flash Lite) | **【究極統合認知カーネル】**<br>動的ギアリング、GoT、MBR、3役自己討論、事前防御バインドを全内包。 |
| **OS更新・管理規約** | **v23.2.0 管理プロトコル** | **OS保守・監査チャット専用** | **【純粋メタ管理レイヤー】**<br>コード出力絶対抑制、3行アンカー差分規格（STRICT_3HEAD_3TAIL_FIXED）準拠。 |

---

### 🚀 使い方

1. **導入**:
   単一マスターコード（YAML版）をコピーし、AIのシステムプロンプト（System Instructions 欄）に設定します。
2. **推奨実行環境**:
   一般向け Web UI のコンテキストスライシング（過去ログ強制切り捨て）を回避するため、生（Raw）コンテキストが保証される **Google AI Studio（aistudio.google.com）** または **API 経由** での運用を強く推奨します。
3. **運用パラメータ（推奨）**:
   - `Temperature`: **`0.0 〜 0.2`**（決定論的推論の固定）
   - `Top_P`: **`0.95`**
4. **起動**:
   システムプロンプト設定後、特別なコマンド入力なしで即座に高密度待機状態（Standby）で起動します。

### ⚠️ 免責事項 (Disclaimer)

* **互換性**: 本システムは **Google Gemini 3 / 3.1 / 3.7 / 3.8 シリーズ** に完全最適化されています。
* **免責**: 本システムは個人の先端実験プロジェクトです。出力の正確性や、利用による損害について開発者は責任を負いません。

### ☕ 開発支援 (Support)

SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。
もしこのシステムがあなたの役に立ち、活動を応援したいと感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://www.buymeacoffee.com/nitagon1)

---
---

## 🇺🇸 English (Summary)

### 🌌 Design Philosophy: Unified Cognitive Kernel & Dynamic Gearing

> **Conclusion: Model-specific prompt switching is obsolete. A single autonomous kernel shifts reasoning depth dynamically based on task complexity.**

v23.3.0 [ AXIOM_PRIME ] completely unifies Pro and Flash variants into a **Single Master Codebase** (~2,550 chars / ~520 tokens) with autonomous 3-stage dynamic gearing.

#### 1. Dynamic Gearing Architecture
* **AERO_LITE:** High-velocity, zero-overhead execution for routine tasks.
* **HYBRID_FLASH:** Context-cached balanced reasoning for standard interactions.
* **TITAN_PRO:** Maximum cognitive recursion (GoT, Adversarial Debate, MBR Selection, Symbolic Constraints) for mission-critical complexity.

#### 2. Advanced Cognitive Axioms (v23.3.0)
* **Epistemic vs. Aleatoric Decomposition:** Differentiates knowledge deficits from task ambiguity.
* **Minimum Bayes Risk (MBR) Selection:** Extracts loss-minimizing consensus solutions across thought graphs.
* **Entropy Velocity Budgeting:** Scales test-time compute dynamically based on convergence velocity.
* **Pre-Execution Safe_Binding:** Eliminates cold-start context drops and pronoun ambiguity before reasoning begins.
* **Anti-Meta Bleed Guard:** Suppresses unprompted internal system lectures during context drops.

### 🚀 Recommended Environment
To bypass consumer web client context slicing, deployment in **Google AI Studio (aistudio.google.com)** or direct API endpoints is strictly recommended with `Temperature: 0.0 - 0.2`.

### ☕ Support Development

If this system has been valuable to you, your support is deeply appreciated.

[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-FF813F?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://www.buymeacoffee.com/nitagon1)
