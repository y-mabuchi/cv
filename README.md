# 業務経歴書

## 基本情報
|key|value|
|---|---|
|名前|馬渕 勇介|
|居住地|静岡県 浜松市|
|Twitter|[@yusukedev](https://twitter.com/yusukedev)|

## 概要

## スキル

### 言語
Golang | React | TypeScript | Terraform

### クラウド

#### GCP
Cloud Run | Cloud Storage | Cloud SQL | Cloud Build | Cloud Scheduler | Cloud Tasks | Cloud Load Balancing | Cloud CDN | Artifact Registry | Google App Engine

## 主な業務経歴

### 業務管理サービスのAPI開発 [Go / GraphQL / Cloud SQL / GCP / GAS] (2021/08〜)
【概要】  
ある監視サービスの統合表示、管理をするBtoB向けサービス

【担当業務】

- GoによるGraphQLサーバ開発
- Cloud BuildによるCD構築
- GitHub ActionsによるCI構築
- SendGridによるメール送信
- Sentry, Datadogによる運用監視の導入
- Terraformによるインフラのコード化
- GraphQLのAPI仕様書自動生成
- ER図の自動生成
- 業務効率化のため、複数リポジトリをモノレポに変更

【発揮したバリュー】  
2021/12〜リーダーエンジニアとして活動
2022/04〜リードエンジニアとして活動

【技術スタック】

#### バックエンド
- Go
- GraphQL
- SQLBoiler
- gqlgen
- golang-migrate

#### フロントエンド
- React
- Next.js
- TypeScript
- Apollo Client
- GraphQL Code Generator

#### クラウドインフラ
- Cloud Run
- Google App Engine
- Cloud SQL
- Cloud Build
- Cloud Scheduler
- Cloud Tasks

#### CI
- GitHub Actions
- SpectaQL
- tbls
- Secretlint

#### 運用監視
- Datadog
- Sentry

#### IaC
- Terraform

【課題】  
現行システムのリプレイスだったものの、仕様変更が開発に遅れが生じるようになったことが課題でした。  

プロジェクトに関わる時間が一番長かったため、ビジネスサイド・フロントエンド・バックエンドを交えたショートミーティングを細かく実施し、仕様や確認事項を洗い出し、Confluenceに記載、情報が集約するようにしました。  

私が情報の集中点となることで、確認事項がスムーズに行われるようになりました。  

【工夫した点】  
- 実データが入った動作確認で速度が遅い部分が多くあったため、クエリを特定し適切なインデックスを設定して解消しました。
- バッチ処理でコンテナが落ちる、クエリが残り続ける、という不具合があったため、Datadog、Sentryを確認し原因となる箇所と調査して解消しました。
- Golangを実務で使うのは初めてだったため、IDEの自動Lint機能を使いフォーマットをきれいに保つ、ファンクションを定義する際は適切にエラーを返すよう設計し、実行時エラーを少なくするよう心がけました。
- Dockerを使って開発していたため、デバッグしづらいという意見を元に、リモートデバッガをプロジェクトに導入し開発の効率化を行いました。
- 環境ごと（dev, stg, prod）に手作業でGCPプロジェクトを作業していたため、Terraformを導入しコードベースでクラウドインフラを管理できるようにしました。
- お客様への納品物としてAPI仕様書やER図が必要だったため、CIで自動生成するように設定し、常に最新の情報が自動で反映されるようにしました。
- フロントエンド、バックエンド、インフラがそれぞれ別のリポジトリで稼働していたため、モノレポに変更し、API駆動開発ができるようにしました。

---

### DocBaseからConfluenceへデータ移行するCLIツール [Go] (2022/03〜)

【概要】  
DocBaseからエクスポートしたJSONファイルを元に、Confluence APIを使用して移行するCLIツール

---

### EC管理画面のE2Eテスト [React / TypeScript / Firebase / Cypress / GitHub Actions] (2022/01〜)
【概要】  
あるEC管理画面のE2Eテスト

【担当業務】
- Firebase Local Emulatorの導入
- Cypressによるテストの自動化導入
- GitHub ActionsによるCI構築

【技術スタック】
- React
- TypeScript
- Firebase
- Cypress
- GitHub Actions

【補足】  
副業での参画です

---

### 地域特化ビジネスマッチングサービス [React / TypeScript / Next.js / Firebase] (2021/09〜2021/12)
【概要】  
ある地域に特化したビジネスマッチングサービス

【担当業務】
- Reactによるコンポーネント作成
- Reactによるページ作成
- react-queryを使用したFirebaseとのつなぎ込み

【技術スタック】
- React
- TypeScript
- Next.js
- react-query
- Firebase

【補足】  
副業での参画です

---

### 動画コンテンツBtoBマッチングサービスのAPI開発 [Go / GraphQL / Cloud SQL / GCP] (2021/07〜2021/08)
【概要】  
動画コンテンツのBtoB向けマッチングサービス

【担当業務】

- GoによるGraphQLサーバ開発

---

### ECサイト開発 [React / TypeScript / Next.js / Firebase] (2021/01〜2021/09)
【概要】  
そば粉を販売するECサイト

【担当業務】
- Firestoreのスキーマ設計
- Reactによるコンポーネント、およびページ開発
- Firebaseとの通信開発

【補足】  
副業での参画です

---

### フードデリバリーサービス開発 [VB.net / TypeScript] (2020/01〜2021/08)

【概要】  
タクシーが飲食店の料理をデリバリーするプラットフォームの企画、開発  

【担当業務】  
企画、基本設計、画面設計、Push通知を行うエンドポイントのコーディング  

【使用技術】
- Cloud Functions
- Firebase Cloud Messaging
- TypeScript
- Figma

【課題】
- コロナ禍によって大幅なダメージを受けた飲食店・タクシー業界の売上減
- 飲食店に行きたくても、コロナ禍により行けない

【工夫した点】  
出発地、目的地を郵便番号で管理し、Google Directions APIを使用して距離を計算、エリア区分をすることで、配送範囲を制御しました  

---

### CMS開発 [React / TypeScript / Next.js / WordPress] (2020/01〜2020/03)
【概要】  
静的サイトジェネレータを使った表示速度の早いCMS  

【担当】  
企画、設計、コーディング  

【使用技術】
- React
- Next.js
- TypeScript
- WordPress

【課題】  
SEO対策を十分に行ったWordPressでは表示速度が犠牲になってしまう

【工夫した点】  
Lighthouseで高得点となるように、Suggestを一つ一つ対応

---

### 社内業務システム開発 [Google Apps Script / TypeScript] (2018/01〜2020/01)
【概要】  
飲食店のバックオフィスを管理する業務システムの設計、構築、運用  
- 売上管理
- シフト管理
- 請求書管理
- 会計ソフトとの連動
- 勤怠管理ソフトとの連動

【担当】  
企画、設計、コーディング、保守

【使用技術】
- Google Apps Script
- TypeScript

【課題】
- 業務を引き継いだ当初、Webエディターで直接コーディングされており、ソースコード管理がされていなかった
- ファイルが適切に分割されておらず、コードの可読性が悪かった
- テストコードが存在しなかった

【工夫した点】
- ライブラリを使用しローカルで開発できるように変更、gitを導入しソースコード管理を行うようにした
- TypeScriptを使用して、ファイルを適切に分割、可読性を高めた
- ユニットテストを導入した

---

### 給与計算システム開発 [Excel VBA] (2016/01〜2016/12)
【概要】  
給与計算システムとのダブルチェックのため、エクセルを使用した給与計算システムの開発  

【担当】  
設計、開発、コーディング、保守  

【使用技術】
- Excel VBA

---

### 日報システム開発 [PHP / MySQL] (2007/01〜2007/12)
【概要】  
顧客検索、日報管理システムの開発  


【担当】  
設計、開発、コーディング、保守  

【使用技術】
- PHP
- MySQL
- Twitter Bootstrap
- Linux
