# 業務経歴書

## 基本情報
|key|value|
|---|---|
|名前|馬渕 勇介|
|居住地|静岡県 浜松市|
|Twitter|[@yusukedev](https://twitter.com/yusukedev)|

## 職務要約
- 2021年9月〜現在:      BULB株式会社 Golangを用いたシステム開発を1年経験
- 2017年2月〜2021年8月: 株式会社こころ GASを用いた社内向けシステム開発を4年経験

## 活かせる経験・知識・技術
- Golangによるアプリケーションの開発
- 3〜5名規模のリードエンジニアを経験（スケジュール管理、工数管理、顧客折衝）
- GCP(Cloud Run, Cloud SQL, Cloud Load Balancing, Cloud Storage)を用いたデプロイの経験
- Cloud SQLのスロークエリからインデックスの再設定によるパフォーマンスチューニング
- C#.netからGolangへのリプレイス経験
- CypressによるE2Eテストの経験

## スキルレベル
|     | 言語環境          | 期間     | レベル                                                        |
|-----|---------------|--------|------------------------------------------------------------|
| 言語  | Golang        | ★1.5年  | 一人でアプリケーション開発ができる                                          |
|     | React         | ★3年    | 一人でアプリケーション開発ができる                                          |
|     | Terraform     | ★0.5年  | 一人でインフラコード化ができる                                            |
|     | Ruby on Rails | 自宅にて半年 | 知識がある                                                      |
|     | PHP           | 自宅にて半年 | 知識がある                                                      |
|     | Java          | 自宅にて半年 | 知識がある                                                      |
| FW  | Laravel       | 自宅にて半年 | 知識がある                                                      |
|     | Kubernetes    | 自宅にて半年 | 知識がある                                                      |
|     | gRPC          | 自宅にて半年 | 知識がある                                                      |
| DB  | MySQL         | ★1年    | 知識がある                                                      |
| OS  | Linux         | ★1年    | インストールから簡単な設定ができる                                          |
| その他 | Docker        | ★1.5年  | 開発向けのローカル設定から、マルチステージビルドを用いたビルド設定ができる                      |
|     | GCP           | ★1年    | gcloudコマンドによる各リソースの構築から、Terraformを使ったインフラコード化ができる          |
|     | AWS           | 自宅にて半年 | 知識がある                                                      |
|     | CI/CD         | ★0.5年  | GitHub Actionsを用いたデプロイ設定、GraphQLのAPIドキュメント自動生成、ER図自動生成ができる |
＊業務経験あり: ★

## 業務経歴

### 2021年9月〜現在: BULB株式会社
■事業内容: 受託開発、自社サービス開発  
■資本金: 3,624万円 売上高: 150百万円 従業員数: 14名 非上場

#### 期間
- 2021年9月〜現在

#### プロジェクト内容
ある監視サービスの統合表示、管理をするBtoB向けサービス  

- GoによるGraphQLサーバ開発
- Cloud BuildによるCD構築
- GitHub ActionsによるCI構築
- SendGridによるメール送信
- Sentry, Datadogによる運用監視の導入
- Terraformによるインフラのコード化
- GraphQLのAPI仕様書自動生成
- ER図の自動生成
- 業務効率化のため、複数リポジトリをモノレポに変更

#### 担当フェーズ
- 要件定義(一部PM補佐として)
- 基本設計(一部PM補佐として)
- 詳細設計
- 実装

#### 環境

##### バックエンド
- Go1.16
- GraphQL
- SQLBoiler
- gqlgen
- golang-migrate

##### フロントエンド
- React17
- Next.js11
- TypeScript4
- Apollo Client
- GraphQL Code Generator

##### クラウドインフラ
- Cloud Run
- Google App Engine
- Cloud SQL(MySQL8.0)
- Cloud Build
- Cloud Scheduler
- Cloud Tasks

##### CI
- GitHub Actions
- SpectaQL
- tbls
- Secretlint

##### 運用監視
- Datadog
- Sentry
- new relic

##### IaC
- Terraform

#### メンバー/役割
- リードエンジニア
- 要員: 6名(PM含む)

#### 発揮したバリュー
- 2021/12〜リーダーエンジニアとして活動
- 2022/04〜リードエンジニアとして活動

#### 課題
現行システムのリプレイスだったものの、仕様変更が開発に遅れが生じるようになったことが課題でした。  

プロジェクトに関わる時間が一番長かったため、ビジネスサイド・フロントエンド・バックエンドを交えたショートミーティングを細かく実施し、仕様や確認事項を洗い出し、Confluenceに記載、情報が集約するようにしました。  

私が情報の集中点となることで、確認事項がスムーズに行われるようになりました。  

#### 工夫した点
- 実データが入った動作確認で速度が遅い部分が多くあったため、クエリを特定し適切なインデックスを設定して解消しました。
- バッチ処理でコンテナが落ちる、クエリが残り続ける、という不具合があったため、Datadog、Sentryを確認し原因となる箇所と調査して解消しました。
- Golangを実務で使うのは初めてだったため、IDEの自動Lint機能を使いフォーマットをきれいに保つ、ファンクションを定義する際は適切にエラーを返すよう設計し、実行時エラーを少なくするよう心がけました。
- Dockerを使って開発していたため、デバッグしづらいという意見を元に、リモートデバッガをプロジェクトに導入し開発の効率化を行いました。
- 環境ごと（dev, stg, prod）に手作業でGCPプロジェクトを作業していたため、Terraformを導入しコードベースでクラウドインフラを管理できるようにしました。
- お客様への納品物としてAPI仕様書やER図が必要だったため、CIで自動生成するように設定し、常に最新の情報が自動で反映されるようにしました。
- フロントエンド、バックエンド、インフラがそれぞれ別のリポジトリで稼働していたため、モノレポに変更し、API駆動開発ができるようにしました。

---

### 2021年1月〜現在: toraco株式会社
■副業での参画

#### 期間
- 2021年7月〜現在

#### プロジェクト内容
あるECサイト管理画面のE2Eテスト  

- Firebase Local Emulatorの導入
- Cypressによるテストの自動化導入
- GitHub ActionsによるCI構築

#### 担当フェーズ
- E2Eテスト

#### 環境
- Firebase
- React
- TypeScript
- Cypress
- GitHub Actions

#### メンバー/役割
- プログラマー

#### 工夫した点
- テストケースが多く、スペックファイルの見通しが悪くなったため、ファイル分割を実施
- 各スペックファイルでログインチェックを行うことで、ファイル毎に実行できるように変更

---

#### 期間
- 2021年9月〜2021年12月

#### プロジェクト内容
ある地域に特化したビジネスマッチングサービス  

- Reactによるコンポーネント作成
- Reactによるページ作成
- react-queryを使用したFirebaseとのつなぎ込み

#### 担当フェーズ
- 実装

#### 環境
- React
- TypeScript
- Next.js
- react-query
- Firebase

#### メンバー/役割
- プログラマー(3名、PM含む)

---

#### 期間
- 2021年1月〜2021年9月

#### プロジェクト内容
そば粉を販売するECサイト  

- Firestoreのスキーマ設計
- Reactによるコンポーネント、およびページ開発
- Firebaseとの通信開発

#### 環境
- React
- TypeScript
- Next.js
- react-query
- Firebase

#### メンバー/役割
- プログラマー(5名、PM含む)

---

### 2017年2月〜2021年8月: 株式会社こころ
■事業内容: 外食事業
■資本金: 500万円 売上高: 100百万円 従業員数: 300名(アルバイト含む) 非上場

#### 期間
- 2020年1月〜2021年8月

#### プロジェクト内容
タクシーが飲食店の料理をデリバリーするプラットフォームの企画、開発  

- Push通知を行うエンドポイント開発

#### 担当フェーズ
- 企画
- 設計
- 実装(一部Push通知部分のみ)

#### 環境
- Cloud Functions
- Firebase Cloud Messaging
- TypeScript
- Figma

#### メンバー/役割
- プログラマー(3名、業務委託含む)

#### 工夫した点
- 出発地、目的地を郵便番号で管理し、Google Directions APIを使用して距離を計算、エリア区分をすることで、配送範囲を制御

---

#### 期間
- 2018年1月〜2020年1月

#### プロジェクト内容
飲食店のバックオフィスを管理する業務システムの設計、構築、運用  

- 売上管理
- シフト管理
- 請求書管理
- 会計ソフトとの連動
- 勤怠管理ソフトとの連動

#### 担当フェーズ
- 企画
- 設計
- 実装
- 運用

#### 環境
- Google Apps Script
- TypeScript

#### 課題
- 業務を引き継いだ当初、Webエディターで直接コーディングされており、ソースコード管理がされていなかった
- ファイルが適切に分割されておらず、コードの可読性が悪かった
- テストコードが存在しなかった

#### 工夫した点
- ライブラリを使用しローカルで開発できるように変更、gitを導入しソースコード管理を行うようにした
- TypeScriptを使用して、ファイルを適切に分割、可読性を高めた
- ユニットテストを導入した

## 資格・スキル
- 日商簿記検定2級