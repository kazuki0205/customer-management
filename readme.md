
# プロジェクト名: 顧客情報管理システム

## 概要
このプロジェクトは、買取業務の簡略化を目的として開発された顧客情報管理システムです。iPadでお客様に会員登録を行ってもらい、データベースに登録された情報をPCで管理できる仕組みを提供します。さらに、買取承諾書に必要事項が自動挿入された状態で印刷できるように設計されています。

## こだわった点
- **フロントエンド**
  - **直感的なデザイン**: お客様が使いやすいように、UIデザインにこだわりました。Reactコンポーネントは再利用可能で、プロップスを活用して効率的に作成しています。
  - **コンポーネント設計**: ボタンや入力フィールドなど、共通部品は使い勝手を重視し、プロップスを通じて柔軟に動作を変更できるようにしました。ボタンには登録・削除など異なる機能を持たせ、バリデーションが通っていない場合は無効化（disable）される仕様にしています。
- **サーバーサイド**
  - **セキュリティ対策**: JWTトークンを用いた認証機能や、SQLインジェクション防止のためのバインド処理を実装しました。RESTful API設計を採用し、効率的なデータのやり取りを実現しています。
  - **ローカル環境の使用**: セキュリティを考慮し、情報漏洩のリスクを減らすため、XAMPP環境でローカル動作するよう設計しました。

## 開発の経緯
このシステムは、買取業務の効率化と業務プロセスの改善を目指して企画・実装されました。開発期間が短かったため、迅速な計画とスピード感のある実装が求められました。開発中はモチベーションを保つためにチームメンバーと密にコミュニケーションを取り、協力して進めました。

## ファイル構成
### profile ディレクトリ
- **public**
  - `index.html`: アプリケーションのメインHTMLファイル。
  - その他: アプリケーションのアイコンや設定ファイル。
- **src**
  - `App.js`: アプリケーションのメインコンポーネント。
  - **components**
    - `Button`: ボタンコンポーネント。`index.jsx` とスタイル `style.module.scss` を含む。
    - `InputText`: 入力フィールドコンポーネント。`index.jsx` とスタイル `style.module.scss` を含む。
    - `LoginCheck`: ログインチェックコンポーネント。`index.jsx` のみ。
    - `css`: 共通スタイルシート。`style.module.css` などを含む。
  - **pages**
    - `adminCustomerDetail`: 顧客詳細ページ。`index.jsx` とスタイル `style.module.scss` を含む。
    - `adminTop`: 管理者トップページ。`index.jsx` とスタイル `style.module.scss` を含む。
    - その他: 各ページはそれぞれの機能に特化したファイルとスタイルを持つ。
  - `index.js`: アプリケーションのエントリーポイント。

### server ディレクトリ
- `server.js`: サーバーサイドのメインスクリプト。APIエンドポイントを定義。
- `package.json`: サーバーの依存関係を管理。

## 使用技術
- **フロントエンド**: React, JavaScript, SCSS
- **バックエンド**: Node.js, Express
- **データベース**: MySQL
- **セキュリティ**: JWTトークン, SQLインジェクション対策

## 苦労した点
1. **開発期間の短さ**: スピーディな実装が求められ、迅速な計画と実行が必要でした。
2. **モチベーションの維持**: 困難な状況でも、チームと密なコミュニケーションをとることで乗り越えました。

## 今後の改善点
- より高度なセキュリティ機能の追加。
- さらにユーザーフレンドリーなUIの追求。
