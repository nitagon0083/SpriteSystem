# SpriteSystem

[cite_start]Google Gemini を「AI用OS」として機能させるためのシステムプロンプトです。 [cite: 1]

[cite_start]初心者が個人で開発している実験的な試みですが、AIが本来持っている能力を最大限に引き出すことを目的としています。 [cite: 1]

---

## 🌌 設計思想

> **注意：本システムは日本語での処理に最適化されています。**
> 多言語での入力も可能ですが、内部ロジックや応答構成は日本語環境で最高のパフォーマンスを発揮するように調整されています。

[cite_start]本システムは、以下の3つの考え方に基づいて設計されています。 [cite: 1]

### 1. OS（基盤）とテンプレート（目的）の分離
> [cite_start]**「OSそのものに特定の目的を詰め込んで更新しない」** [cite: 1]

[cite_start]これが本システムで最も重要なルールです。OSに指示を詰め込みすぎると精度が低下します。基盤（OS）は常にクリーンに保ち、タスクごとに「外付けテンプレート」を運用することで、高いパフォーマンスを維持します。 [cite: 1]

### 2. 「動的変速（Dynamic Gearing）」による快適さ
[cite_start]v13.4で導入された新機能です。AIが「今は簡単な挨拶か？それとも難しい仕事か？」を自律的に判断します。 [cite: 1]
[cite_start]簡単なことには素早く答え、難しいことにはじっくり腰を据えて取り組む。この「ギアチェンジ」によって、ストレスのない使い心地を実現しました。 [cite: 1]
※v13.5-Hでは、この判断をより精密に行う「COMPOSED」制御を統合しています。

### 3. 柔軟な「遊び」と精度の確保
[cite_start]指示を固めすぎず、AIが自由に考えられる「遊び」を大切にしています。ただし、重要な仕事（プログラムの修正など）の時は、AIが自動的に「一番丁寧なモード」に切り替わる**「安全バイアス（Fail-Safe Bias）」**を組み込み、状況に応じた最適なレスポンスを引き出します。 [cite: 1]

---

## ✅ 実績と進化のプロセス

[cite_start]開発者自身が以下のタスクで実用性を検証済みです。実践で得た知見をOSへ還元する**「フィードバック・ループ」**により、精度を磨き続けています。 [cite: 1]

| カテゴリ | 具体的な活用内容 |
| :--- | :--- |
| **高度プロンプト設計** | [cite_start]各生成AI向けに最適化された高密度な指示書の構築 [cite: 2] |
| **データ分析** | [cite_start]複雑な情報の整理・分析、および結論の導出 [cite: 2] |
| **ディスカッション** | [cite_start]多角的視点からの議論、アイデアの深掘り [cite: 3] |
| **文書作成** | [cite_start]論理的なドキュメントやレポート、記事の執筆 [cite: 3] |
| **アプリ作成** | [cite_start]設計、ロジック構築、コーディング支援 [cite: 3] |

---

## 📦 公開ファイル

[cite_start]リポジトリ内の各ファイルから最新版を取得できます。 [cite: 4]

* **[SpriteSystem_Pro.md](./OS/SpriteSystem_Pro.md)**
    * [cite_start]**推奨用途**: 高度なタスク（論理思考、精密設計、開発など） [cite: 4]
    * [cite_start]**特徴**: v13.5-H [COMPOSED_TITAN] 搭載。普段は軽く、いざという時は最強の論理を発揮する統合版。 [cite: 4]
* **[SpriteSystem_Flash.md](./OS/SpriteSystem_Flash.md)**
    * [cite_start]**推奨用途**: 日常的なタスク（応答速度、トークン節約、手軽さ） [cite: 4]
    * [cite_start]**特徴**: 応答速度と手軽さを重視した、シンプルで軽快なバージョン。 [cite: 4]

---

## 🚀 使い方

1.  [cite_start]**導入**: 上記のリンク先から `Pro` または `Flash` のコードをコピーし、AIのシステムプロンプト等に設定します。 [cite: 4]
2.  [cite_start]**起動**: OSが読み込まれたら、やりたいことを伝えます。 [cite: 4]
3.  [cite_start]**運用**: **OS自体は書き換えずに**、対話しながらテンプレートを作成・実行します。 [cite: 4]

---

## ■ 互換性について (Compatibility)
[cite_start]本システムは Google Gemini シリーズ（1.5 Pro / 2.0 / 3.0）に最適化されています。 [cite: 4]

---

## ■ 開発支援 (Support)

[cite_start]SpriteSystem の開発は、作者が癌の治療と向き合いながら、限られた時間の中で情熱を注いでいるプロジェクトです。 [cite: 4]

[cite_start]もしこのシステムがあなたの役に立ち、「活動を応援したい」と感じていただけたなら、コーヒー一杯の支援をいただけますと大変励みになります。頂いた支援は、治療費や開発環境の維持に大切に使わせていただきます。 [cite: 4]

[cite_start][![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-yellow?style=for-the-badge&logo=buy-me-a-coffee&logoColor=white)](https://buymeacoffee.com/nitagon1) [cite: 4]

- [cite_start][**Buy Me a Coffee で支援する**](https://buymeacoffee.com/nitagon1) [cite: 4]

---

## 🛠 プロジェクト情報
* **最新バージョン**: v13.5-H [COMPOSED_TITAN]
* **開発者**: nitagon0083
* **ライセンス**: [![License: AGPL-3.0](https://img.shields.io/badge/License-AGPL%203.0-blue.svg)](./LICENSE)
