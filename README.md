# BPMN Editor (bpmn-js)

## 概要

ブラウザだけで動く **bpmn-js** ベースの BPMN 2.0 エディタです。Activiti / Flowable / Camunda 系の拡張属性も保持したまま読み込み・編集・再エクスポートが可能です。

## 特徴

- **完全クライアントサイド** … サーバー不要で動作、ビルド手順も不要
- **ドラッグ & ドロップ対応** … `.bpmn` / `.xml` ファイルを画面に投下するだけ
- **新規作成 / XML 保存 / SVG 保存** ボタン付き
- リポジトリ直下に `allocation-auto.bpmn20.xml` があれば **自動ロード**
- キーボードショートカット (Delete, Ctrl/Cmd+Z など) 標準サポート

> TIP: **Save BPMN** では任意のファイル名を入力できるため、`allocation-auto.bpmn20.xml` を1から作成可能です。

## デモ

```
# クローン & 起動 (例: Python HTTP server)
$ git clone <this-repo-url>
$ cd <repo>
$ python -m http.server 8080
# ブラウザで http://localhost:8080/index.html を開く
```

静的ホスティング (GitHub Pages / Vercel / S3 等) に `index.html` を置くだけでも動きます。

## 使い方

| UI                  | 説明                                     |
| ------------------- | ---------------------------------------- |
| 📂 **ファイル選択** | `.bpmn` / `.xml` を読み込み              |
| ➕ **New Diagram**  | 空の BPMN 図を生成                       |
| ➕ **New allocation-auto.bpmn20.xml** | 空図を生成し保存名を `allocation-auto.bpmn20.xml` に設定 |
| 💾 **Save BPMN**    | ファイル名を指定して BPMN をダウンロード |
| 🖼 **Save SVG**      | SVG 画像をダウンロード                   |

> TIP: `#canvas` にファイルをドラッグ & ドロップしても読み込めます。

## ファイル構成

```
├─ index.html            # メイン HTML (エディタ本体)
└─ allocation-auto.bpmn20.xml  # サンプル BPMN (任意)
```

## 依存ライブラリ

| ライブラリ | バージョン | 用途                          |
| ---------- | ---------- | ----------------------------- |
| bpmn-js    | 18.6.2     | BPMN モデラー本体 (UNPKG CDN) |

## カスタマイズ

- **プロパティパネル追加**: `bpmn-js-properties-panel` を読み込んで `propertiesPanel` モジュールを inject
- **カスタム要素**: Moddle 拡張とカスタムレンダラーを定義すれば独自拡張を描画可能

## ライセンス

MIT
