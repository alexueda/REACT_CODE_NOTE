📖 **推奨読書**:
- [MDN Reactの導入チュートリアル](https://developer.mozilla.org/ja/docs/Web/JavaScript)
- [Reactクイックスタート](https://reactjs.org/docs/getting-started.html)

## Reactとは？

Reactとその関連プロジェクトは、強力なウェブプログラミングフレームワークを提供します。Reactの名前は、ユーザーの操作やデータの変化に基づいて、自動的に更新される「リアクティブな」ウェブページコンポーネントを構築することに由来します。

---

### 創設者 Jordan Walkeの言葉

> "The best drug is getting little things done that have been weighing on you. Instant high."
> 
> — Jordan Walke（出典: Twitter）

---

## Reactの歴史

Reactは2011年、Jordan WalkeによってFacebookで使用するために作成されました。最初にFacebookのニュースフィードで使用され、その後Instagramの主要フレームワークとして採用されました。間もなくしてFacebookはReactをオープンソース化し、多くの人気ウェブアプリケーションに採用されるようになりました。

## Reactの特徴 - JSXとBabel

Reactは、HTMLをJavaScriptのバリアント（派生）であるJSXに抽象化します。JSXは、Babelというプリプロセッサによって有効なHTMLとJavaScriptに変換されます。

### JSXの例

以下はJSXファイルの例です。HTMLとJavaScriptが一つの表現に混ざっていることがわかります。

```jsx
const i = 3;
const list = (
  <ol class='big'>
    <li>Item {i}</li>
    <li>Item {3 + i}</li>
  </ol>
);
```

このコードは、Babelによって次のような有効なJavaScriptコードに変換されます：

```javascript
Copy code
const i = 3;
const list = React.createElement(
  'ol',
  { class: 'big' },
  React.createElement('li', null, 'Item ', i),
  React.createElement('li', null, 'Item ', 3 + i)
);
```

##Reactのリアクティブな仕組み

React.createElement関数はDOM要素を生成し、それらが表すデータの変更を監視します。変化が検出されると、Reactは依存する変更を自動でトリガーします。こうしてReactは効率的にリアクティブなUIを提供します。
