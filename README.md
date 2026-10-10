# JAL搭乗記録 PWA

FOP・LSPを記録・集計するPWA（Progressive Web App）です。

## GitHub Pages での公開手順

1. GitHubで新規リポジトリを作成（Public）
2. `index.html` / `manifest.json` / `sw.js` / `icon-180.png` / `icon-512.png` をアップロードして Commit
3. Settings → Pages → Source: Deploy from a branch / Branch: `main` `/ (root)` を選択して Save
4. 1〜2分後に `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開されます

## iPhoneでのインストール

Safariで公開URLを開く → 共有ボタン →「ホーム画面に追加」

## データについて

- データは端末のブラウザ（localStorage）に保存されます。サーバーには送信されません
- 初回起動時に、埋め込み済みのバックアップ（2026-10-10時点）が自動で読み込まれます（以降の編集内容は保持されます）
- 機種変更の際は、アプリ内のエクスポートでJSONを保存 → 新環境でインポートしてください

## 更新方法

`index.html` を上書きアップロードするだけです。Service Workerはネットワーク優先のため、次回オンライン起動時に自動更新されます。
