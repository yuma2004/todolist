# Express.js の基本

## Express.js の概要

Express.jsは、Node.jsのための軽量なWebアプリケーションフレームワークです。簡単にAPIを構築できるように設計されており、ルーティング、ミドルウェアのサポート、豊富なHTTPユーティリティなどが含まれています。これにより、効率的にWebサーバーを構築することが可能になります。

### Expressのインストール

Expressを使用する前に、Node.jsがインストールされている必要があります。その後、以下のコマンドでExpressをプロジェクトに追加できます。

npm install express

### 最初のExpressアプリケーション

Expressを使って基本的なWebサーバーを構築する例を以下に示します。

const express = require('express');
const app = express();

app.get('/', (req, res) => {
  res.send('Hello World!');
});

const port = 3000;
app.listen(port, () => {
  console.log(`App listening at http://localhost:${port}`);
});

このコードは、ポート3000でサーバーを起動し、ルートURLにアクセスした際に'Hello World!'を表示します。

## Expressの主な特徴

- **ルーティング**: URLごとに異なるルートハンドラを簡単に設定できます。
- **ミドルウェア**: リクエストとレスポンスの間に処理を挟むことができます。これにより、機能拡張やコードの再利用が容易になります。
- **エラーハンドリング**: 開発者はエラー処理ルーチンを簡単に組み込むことができます。
- **サードパーティミドルウェアのサポート**: 様々なサードパーティミドルウェアを利用して、アプリケーションを拡張できます。

Expressはそのシンプルさと柔軟性から、Node.jsを使用したWeb開発において非常に人気があります。続いて解説する技術やその他の要望があれば教えてください。
