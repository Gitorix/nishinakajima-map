# 西中島南方マップ（GitHub Pages 用）

このフォルダはそのまま GitHub リポジトリにアップすれば、`index.html` がトップページとして公開されます。

## 公開手順（GitHub Pages）
1. GitHub に新規リポジトリを作成（例: `nishinakajima-map`）。
2. このフォルダの中身（`index.html` と `extras/`、`README.md`）をそのリポジトリの **main ブランチ**直下にアップロードしてコミット。
3. リポジトリ画面の **Settings → Pages** を開き、**Source: Deploy from a branch** を選択。  
   **Branch: main** / **Folder: /**（root）を選んで **Save**。
4. リポジトリの上部にサイト URL が表示されるので、それを開くと `index.html` が表示されます。

> 既に `username.github.io` 形式のリポジトリを使っている場合は、そこに `index.html` を置いても OK です。

## 使い方・カスタム
- 画像差し替え：`index.html` の `<script>` 内、`places` 配列の `img` を任意の画像 URL に変更。
- 店の追加/削除：同じく `places` 配列のオブジェクトを追加/削除。
- 初期表示位置：`setView([lat, lng], zoom)` の数値を変更。
- カード表示を最小化：画面右下の「隠す」ボタンで折りたたみ可。

## 注意
- タイルとライブラリは CDN（OSM/Leaflet）から読み込む構成です。ネット接続が必要です。
- `extras/` 配下に他のバリエーションの HTML を同梱しています。トップにしたい場合はファイル名を `index.html` に差し替えてください。
