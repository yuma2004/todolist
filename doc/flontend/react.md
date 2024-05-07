# React.js の基本

## React.js の導入

Reactは、ユーザーインターフェースを構築するためのJavaScriptライブラリです。Facebookが開発し、効率的かつ再利用可能なUIコンポーネントを作成することができます。

### Reactのインストール

Reactプロジェクトを始めるためには、Node.jsがインストールされている必要があります。その上で、Create React Appを利用して新しいプロジェクトを簡単にセットアップできます。

npx create-react-app my-app
cd my-app
npm start

このコマンドは、名前がmy-appの新しいReactアプリケーションを作成し、開発サーバーを起動します。

## コンポーネントの作成

Reactでは、すべてのUI部分はコンポーネントとして表されます。コンポーネントは、classまたはfunctionを使って定義できます。

### 関数コンポーネント

function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

このコンポーネントは、propsとしてnameを受け取り、メッセージを表示します。

### クラスコンポーネント

class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}

クラスコンポーネントは、ライフサイクルメソッドを利用する場合や、内部状態を持つ場合に便利です。

## 状態管理

ReactのuseStateフックを使って、関数コンポーネント内で状態を管理することができます。

import React, { useState } from 'react';

function Counter() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}

この例では、countという状態を持ち、ボタンをクリックするたびにその値を更新します。

## プロップスとコンポーネントの合成

コンポーネントは他のコンポーネントを含むことができ、propsを通じてデータを渡すことができます。

function App() {
  return (
    <div>
      <Welcome name="Sara" />
      <Welcome name="Cahal" />
      <Welcome name="Edite" />
    </div>
  );
}

このAppコンポーネントは、異なるnameプロップスを持つ複数のWelcomeコンポーネントをレンダリングします。


