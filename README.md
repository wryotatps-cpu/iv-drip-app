# 点滴滴下シミュレーター

輸液量・輸液時間・1mLあたりの滴下数から、1分あたりの滴下数を自動計算し、
点滴筒のアニメーションでリアルタイムに表示するWebアプリです。

## 特徴

- **完全無料** — GitHub Pages で無料公開
- **オフライン対応** — Service Worker により、一度アクセス後はオフラインでも動作
- **ホーム画面に追加可能** — PWA対応のため、スマートフォンのホーム画面にアイコンとして追加可能
- **フレームワーク不要** — HTML / CSS / JavaScript のみで構築

## ファイル構成

```
iv-drip-app/
├── index.html      # アプリ本体
├── manifest.json   # PWA設定ファイル
├── sw.js           # Service Worker（オフライン対応）
├── icon-192.png    # アプリアイコン（192×192px）※要作成
├── icon-512.png    # アプリアイコン（512×512px）※要作成
└── README.md       # このファイル
```

## GitHub Pages への公開手順

### 1. GitHubアカウント作成（未作成の場合）
https://github.com にアクセスして無料アカウントを作成

### 2. 新しいリポジトリを作成
1. GitHub にログイン後、右上の「+」→「New repository」
2. Repository name に任意の名前を入力（例：`iv-drip-app`）
3. 「Public」を選択
4. 「Create repository」をクリック

### 3. ファイルをアップロード
1. リポジトリページで「uploading an existing file」をクリック
2. このフォルダ内のファイルをすべてドラッグ＆ドロップ
3. 「Commit changes」をクリック

### 4. GitHub Pages を有効化
1. リポジトリの「Settings」タブをクリック
2. 左メニューの「Pages」をクリック
3. Source を「Deploy from a branch」に設定
4. Branch を「main」、フォルダを「/ (root)」に設定
5. 「Save」をクリック
6. 数分後に `https://ユーザー名.github.io/iv-drip-app/` で公開完了

## アイコンについて

`icon-192.png`（192×192px）と `icon-512.png`（512×512px）を用意すると、
スマートフォンのホーム画面に追加した際にアイコンが表示されます。
アイコンが不要な場合は、`manifest.json` の `icons` セクションを削除してください。

## 計算式

```
1分あたりの滴下数（滴/分）= 輸液量（mL）× 1mLあたりの滴下数（滴/mL）÷ 輸液時間（分）
```

## ライセンス

自由に使用・改変・配布可能です。
