## Masao Iwamoto (@gantaro-max)
 
**業務課題を、自分で設計して自分で作る。医療ドメイン35年 × AI駆動開発。**
 
医薬品卸売業界に35年在籍し、医療系システムの導入・保守を11年担当してきました。
現在は現場の課題をコードで解決しています。
 
- 毎日3〜4時間の手作業だった実績集計を全自動化(**年間約800時間の削減**)
- 業務用Webアプリを要件定義から一人で内製
- Findy スキル偏差値 **68**
---
 
### つくったもの
 
| リポジトリ | 概要 | 技術 |
|---|---|---|
| **[account-target-manager](https://github.com/gantaro-max/account-target-manager)** | 階層型BtoB営業ターゲット管理ツール(SFA/CRM)。実務で内製した案件管理アプリを業種非依存に汎化。インフラを持たずGoogleアカウントだけで動くことを制約条件に設計 | GAS / スプレッドシート / Chart.js |
| **[stamp-rally](https://github.com/gantaro-max/stamp-rally)** | LINE Bot + LIFF のスタンプラリー。**Renderで本番稼働、実イベント(約20名)で運用。** 公式SDKを使わずWebhook署名検証・IDトークン検証を自前実装 | Rust / Axum / sqlx / TiDB / Docker |
| **[quotation-app](https://github.com/gantaro-max/quotation-app)** | 見積作成・保存システム。過去見積の複製、Gemini APIによる見積書のOCR自動読取 | Spring Boot / React / TypeScript / MyBatis |
| **[mysterybot](https://github.com/gantaro-max/mysterybot)** | 謎解きイベントプラットフォーム。1システムで複数イベントを同時稼働させるマルチテナント方式 | Java 21 / Spring Boot 4 / Spring Security |
 
いずれも2025年8月のJava学習開始以降、約1年で構築したものです。
stamp-rally は着手から**約2ヶ月**で本番稼働に到達しました。
 
---
 
### AIに書かせたコードを、どう検証可能にするか
 
AIに実装させること自体は誰でもできます。難しいのは**品質をどう担保するか**です。
私は開発フローそのものを設計し、テンプレート化して公開しています。
 
**設計するAIと実装するAIを分離し、間に実装指示書を挟む**
 
設計と実装を同じAIが続けて行うと、仕様が会話ログの中にしか残りません。
実装が仕様通りかを検証する基準そのものが失われます。
書面を挟むことで、正しさの判定が「動くかどうか」から「**書面と一致するかどうか**」に変わります。
 
**レビュー観点は、照合先ドキュメント(SSOT)の数から導出する**
 
観点を先に決めるのではなく、SSOTの数だけレビュー担当を立てる。
この体制で、指示どおり実装されていながら設計上は誤っている実装
(Webhookの並行処理による順序崩れ、認証試行制限の競合状態)を実際に検出・差し戻しました。
 
**限界も書いています**
 
ドキュメントに書かれていない不変条件は、担当エージェントが存在しないため検証されません。
これは欠陥ではなく、SSOTを書き足す動機として機能させています。
 
→ 詳細・テンプレート一式:[account-target-manager / 開発プロセス](https://github.com/gantaro-max/account-target-manager#開発プロセス指示書駆動--多エージェントレビュー)
 
---
 
### 技術
 
- **実務(2023年〜)** Python(Playwright / Pandas)、Google Apps Script、JavaScript
- **個人開発(2025年8月〜)** Rust(Axum / sqlx / Tokio)、Java(Spring Boot 3 / 4、Spring Security、MyBatis)、React / TypeScript、MySQL / TiDB、Docker、Render
- **プロセス** TDD、指示書駆動開発、多エージェントレビュー、Git / GitHub
- **資格** 基本情報技術者(2001年)
 
---
 
### 経歴
 
医薬品営業(開業医・病院担当)→ 医療機器・医療用システムの販売促進 → 医療系システムの導入・保守(11年、電子カルテ連携の仕様調整を含む)→ 業務改善・内製開発。
 
医療機関・調剤薬局の業務と、電子カルテをはじめとする医療ITの実情を、現場の言葉と技術の言葉の両方で理解しています。
