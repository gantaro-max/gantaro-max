## Masao Iwamoto (@gantaro-max)

**業務を聞き取り、要件を整理し、使われる仕組みにする。医療IT 11年 × 業務改善・内製開発。**

医薬品卸売業界に35年在籍し、医療系システムの導入・保守を通算11年担当してきました。
現在は現場の業務課題を Python・GAS などで仕組みに変え、導入・運用まで担当しています。

- 前任者から引き継ぎ、自身が毎日3〜4時間かけていた実績集計を Python で全自動化
  (**年間約800時間の削減**。従来の作業時間を年換算した概算です)
- 業務用Webアプリを、利用者へのヒアリング・要件定義から導入・運用・改修まで担当
- Rust製のLINE Botを、着手から**約2ヶ月で本番稼働**させ、実際のイベントで運用

---

### つくったもの(主なもの)

| リポジトリ | 概要 | 技術 |
|---|---|---|
| **[account-target-manager](https://github.com/gantaro-max/account-target-manager)** | 階層型BtoB営業ターゲット管理ツール(SFA/CRM)。実務で内製した案件管理アプリを業種非依存に汎化。インフラを持たずGoogleアカウントだけで動くことを制約条件に設計 | GAS / スプレッドシート / Chart.js |
| **[stamp-rally](https://github.com/gantaro-max/stamp-rally)** | LINE Bot + LIFF のスタンプラリー。**Renderで本番稼働、実イベント(約20名)で運用。** 公式SDKを使わない構成で、Webhook署名検証・IDトークン検証を実装 | Rust / Axum / sqlx / TiDB / Docker |
| **[quotation-app](https://github.com/gantaro-max/quotation-app)** | 見積作成・保存システム。過去見積の複製、Gemini APIによる見積書のOCR自動読取。実運用しながら改修を継続 | Spring Boot / React / TypeScript / MyBatis |
| **[mysterybot](https://github.com/gantaro-max/mysterybot)** | 謎解きイベントプラットフォーム。1システムで複数イベントを同時稼働させるマルチテナント方式 | Java 21 / Spring Boot 4 / Spring Security |

いずれも2025年8月のJava学習開始以降、約1年で構築したものです。
上の4件には、実務で内製したアプリを汎化した account-target-manager を含みます。
4件の独立した商用開発実績という意味ではありません。
このほかに学習用・趣味のリポジトリを公開しています。

---

### AI活用と、担当した範囲

**要求・設計判断・動作確認・最終承認は私が担当し、設計書・指示書の起案、コード生成、レビューに
AIコーディングエージェント(Claude / Codex)を活用しています。**

設計するAIと実装するAIを分け、間に実装指示書を挟んでいます。
設計と実装の判断を会話だけに残すと、仕様と成果物を照合しにくくなるため、
仕様と判断理由を文書に残しています。この体制で、指示どおり実装されていながら
設計上は誤っている実装(Webhookの並行処理による順序崩れ、認証試行制限の競合状態)を
検出し、差し戻しました。

ドキュメントにない条件は、レビューで見落とす可能性があります。
文書との照合だけで十分とは考えず、動作確認で見つけた条件も文書とテストに反映しています。

→ 詳細・テンプレート一式:[account-target-manager / 開発プロセス](https://github.com/gantaro-max/account-target-manager#開発プロセス指示書駆動--多エージェントレビュー)

MysteryBot は、2026年1月までの初期実装を自分で行い(チャットAIに相談し、仕上げにAIのコードも使用)、
6月の改修でAIエージェントを活用しました。全リポジトリに同じ分担を当てはめてはいません。

---

### 技術

**実務(2023年〜)** Python(Playwright / Pandas・自身で実装)、Google Apps Script / JavaScript(日報は自身で初版実装+AI改修、案件管理は対話AIからエージェントへ移行)
**個人開発(Java学習2025年8月〜、AIエージェント活用は同年12月以降、Rustは2026年7月〜)** Rust(Axum / sqlx / Tokio)、Java(Spring Boot 3 / 4、Spring Security、MyBatis)、React / TypeScript、MySQL / TiDB、Docker、Render
**プロセス** TDD、指示書駆動開発、多エージェントレビュー、Git / GitHub

**資格** 基本情報技術者(2001年)/ RaiseTech Javaコース修了(2025年12月)

---

### 経歴

医薬品営業(1991〜2001年)、医療IT導入・保守(2001〜2011年・2014〜2015年、通算11年)、販売促進(2011〜2014年・2015年以降)を経験。2023年以降は部署の実績管理・サポートのほか、依頼に応じた業務アプリ開発も担当しています。

医療機関・調剤薬局の業務と、電子カルテをはじめとする医療ITの実情を、現場の言葉と技術の言葉の両方で理解しています。
