# ToDoリストアプリ開発ドキュメント

## プロジェクト概要
ToDoリストアプリケーションの開発に関する技術的な詳細と分担について。

# ToDoリストアプリの画面定義

## 1. ログイン画面 / サインアップ画面
- ユーザーがアカウントを持っていない場合はサインアップを促します。
- ユーザーが既にアカウントを持っている場合はログインを促します。

## 2. ダッシュボード画面
- ログイン後に表示される主要な画面です。
- ユーザーの全てのToDoリストを表示します。
- 新しいリストを追加するオプション、および各リストを編集・削除するオプションがあります。
- 各リストをクリックすると、そのリストの詳細ページに移動します。

## 3. リスト詳細画面
- 選択したリストに含まれる全タスクを表示します。
- タスクを追加、編集、削除するオプションがあります。
- タスクを検索する機能も含まれます。

## 4. 通知画面
- ユーザーが設定したタスクの期限が近づいている場合に通知を受け取ることができます。

## 5. プロファイル設定画面
- ユーザーが自分のアカウント情報（パスワード、メールアドレス等）を編集できる画面です。


## フロントエンド

### 技術スタック
- React.js
- Redux/Context API
- Axios/Fetch
- WebSocket (socket.io-client)
- Formik + Yup
- Jest
- React Testing Library
- Cypress

### コンポーネント分担
1. **ログイン/サインアップページ**
   - 認証フォームのUI実装
   - Axios/Fetchを使用してAPIからJWTトークンを取得
   - React Routerで認証後のリダイレクトを管理

2. **ダッシュボード**
   - リストのCRUD UIの実装
   - ReduxまたはContext APIを使った状態管理

3. **リスト詳細ページ**
   - タスク表示と操作のReactコンポーネント
   - moment.jsで日付処理

4. **検索機能**
   - デバウンス機能を持つ検索バーの実装
   - lodash.debounceを使用

5. **通知機能**
   - WebSocketsまたはPollingを使用したリアルタイム通知
   - socket.io-clientでWebSocket通信

6. **プロファイル設定ページ**
   - ユーザー情報の更新UI
   - FormikとYupでのフォームバリデーション

## バックエンド

### 技術スタック
- Node.js
- Express.js
- MongoDB/PostgreSQL
- JWT
- Bcrypt
- Mongoose/Sequelize
- Elasticsearch
- Node-cron
- Node-schedule
- Jest
- Supertest
- Artillery/JMeter

### API分担
1. **ユーザー認証API**
   - ユーザー登録とログインのAPI実装
   - Bcryptでパスワードのハッシュ化、jsonwebtokenでトークンの発行

2. **リスト管理API**
   - CRUD操作の実装
   - MongooseまたはSequelizeを使用

3. **タスク管理API**
   - CRUD操作のAPI実装
   - express-async-errorsでエラーハンドリング

4. **検索API**
   - Elasticsearchを利用した検索機能の実装

5. **通知API**
   - node-cronで定期実行
   - node-scheduleで通知ロジックの実装

6. **ユーザープロファイルAPI**
   - ユーザー情報の安全な更新

## デプロイ

### フロントエンド
- ツール: Netlify/Vercel
- 自動CI/CDを使用したデプロイ

### バックエンド
- ツール: Heroku/AWS Elastic Beanstalk
- 環境変数とデータベース接続の設定

## テスト戦略

### フロントエンド
- ユニットテスト: Jest + React Testing Library
- 統合テスト: React Testing Library
- E2Eテスト: Cypress

### バックエンド
- ユニットテスト: Jest
- 統合テスト: Supertest
- 負荷テスト: Artillery/JMeter

