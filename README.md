# my-extension

**my-extension** は、Chrome で動作するシンプルな拡張機能です。この拡張機能では、ツールバーのアイコンをクリックするとポップアップ画面が表示されます。

### フォルダ構成

```
my-extension/
├── manifest.json  # 拡張機能の設定ファイル
├── popup.html     # ポップアップのHTML
└── popup.js       # ポップアップで動作するJavaScript
```

### 機能

- ツールバーアイコンをクリックすると、`popup.html` が表示されます。
- ポップアップ画面に追加されたボタンをクリックすると、簡単な動作（アラート）を行います。

---

### インストール方法

1. Chrome を開き、アドレスバーに以下を入力してアクセスします：
   ```
   chrome://extensions/
   ```

2. 右上の「デベロッパーモード」をオンにします。

3. 「パッケージ化されていない拡張機能を読み込む」をクリックし、このフォルダを選択します。

4. ツールバーに表示された拡張機能アイコンをクリックして動作を確認します。

---

### 使用方法

1. 拡張機能のアイコンをクリックします。
2. ポップアップ画面に表示されたボタンをクリックすると、以下のようなアラートが表示されます：
   ```
   Hello, world!
   ```

---

### ファイルの内容

#### `manifest.json`
拡張機能の設定を定義するファイル。

```json
{
    "manifest_version": 3,
    "name": "First Extension",
    "version": "1.0",
    "description": "これは初めての拡張機能です。",
    "action": {
      "default_popup": "popup.html"
    }
  }
```

#### `popup.html`
ポップアップ画面のHTML。

```html
<!DOCTYPE html>
<html>
<head>
  <title>My Extension</title>
</head>
<body>
  <h1>Hello, Chrome Extension!</h1>
  <button id="click-me">Click me</button>
  <script src="popup.js"></script>
</body>
</html>
```

#### `popup.js`
ポップアップ内で動作するJavaScript。

```javascript
document.getElementById("click-me").addEventListener("click", () => {
    alert("Hello, world!");
  });
```

---

### ライセンス

このプロジェクトは自由に利用できます。ただし、著作権表示を残してください。
