# JAL搭乗記録 PWA

FOP・LSPを記録・集計するPWA（Progressive Web App）です。

## GitHub Pages での公開手順

1. GitHubにログインし、右上の「+」→「New repository」で新しいリポジトリを作成
   - Repository name: 例 `jal-flight-log`
   - Public を選択（Privateの場合、Pagesは有料プランが必要）
2. 「uploading an existing file」リンク（または Add file → Upload files）から、以下の5ファイルをすべてアップロードして Commit
   - `index.html` / `manifest.json` / `sw.js` / `icon-180.png` / `icon-512.png`
3. リポジトリの Settings → Pages を開く
   - Source: 「Deploy from a branch」
   - Branch: `main` / フォルダ: `/ (root)` を選択して Save
4. 1〜2分待つと `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開される
   （Pages画面上部に公開URLが表示されます）

## iPhoneでのインストール

1. Safariで公開URLを開く
2. 共有ボタン →「ホーム画面に追加」
3. ホーム画面のアイコンから起動（スタンドアロン表示・オフライン起動対応）

## データについて

- データは端末のブラウザ（localStorage）に保存されます。サーバーには送信されません
- 初回起動時に、埋め込み済みのバックアップ（2026-08-24時点）が自動で読み込まれます
- 以降の編集内容はそのまま保持されます（バックアップで再上書きされることはありません）
- 機種変更・ブラウザ変更の際は、アプリ内のエクスポート機能でJSONを保存 → 新環境でインポートしてください

## 更新方法

`index.html` を修正したら、リポジトリに上書きアップロード（同名ファイルをUpload files）するだけです。
Service Workerはネットワーク優先のため、次回オンライン起動時に自動で新しい版に更新されます。
