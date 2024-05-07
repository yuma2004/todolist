CSSの基本
CSS（Cascading Style Sheets）は、HTMLやその他のマークアップ言語で作成されたウェブページのプレゼンテーション（スタイル）を指定するための言語です。

```css
body {
    font-family: Arial, sans-serif;
    color: #333333;
}

h1 {
    color: #1155cc;
}

p {
    margin: 20px 0;
    line-height: 1.6;
}
```

このCSSは、body タグのフォントファミリーと色を設定し、h1 タグのテキスト色を指定し、p タグのマージンと行間を設定しています。

HTMLにCSSを適用する方法
    インラインスタイル:
    直接HTML要素にスタイルを適用します。
```html
<p style="color: red;">これは赤いテキストの段落です。</p>
```

内部スタイルシート

```css
<style>
h1 { color: blue; }
</style>
```

```html
<link rel="stylesheet" href
```