# Node.js の基本

## Node.js の概要

Node.jsは、JavaScriptをサーバーサイドで実行するためのプラットフォームです。Google ChromeのV8 JavaScriptエンジン上で動作し、非同期型のイベント駆動アーキテクチャを採用しているため、高性能なアプリケーションの開発が可能です。

### Node.jsのインストール

Node.jsは公式サイトからダウンロードしてインストールできます。インストール後、コマンドラインでnode -vを実行し、バージョン情報が表示されればインストール成功です。

公式サイト: https://nodejs.org/

### 最初のNode.jsアプリケーション

Node.jsで簡単なHTTPサーバーを作成する例を以下に示します。

const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

const port = 3000;
server.listen(port, () => {
  console.log(`Server running at http://localhost:${port}/`);
});

このスクリプトをserver.jsとして保存し、node server.jsコマンドで実行することでサーバーが起動し、ブラウザからhttp://localhost:3000を開くと'Hello World'が表示されます。

## Node.jsの主な用途

- Webサーバーの構築
- APIの開発
- リアルタイム通信アプリケーション
- ユーティリティスクリプトの作成

Node.jsはそのスケーラビリティと高性能により、多くの企業で採用されています。
