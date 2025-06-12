# BPMN Editor (bpmn-js)

## 概要

ブラウザだけで動く **bpmn-js** ベースの BPMN 2.0 エディタです。Activiti / Flowable / Camunda 系の拡張属性も保持したまま読み込み・編集・再エクスポートが可能です。

## 特徴

- **完全クライアントサイド** … サーバー不要で動作、ビルド手順も不要
- **ドラッグ & ドロップ対応** … `.bpmn` / `.xml` ファイルを画面に投下するだけ
- **新規作成 / XML 保存 / SVG 保存** ボタン付き
- リポジトリ直下に `allocation-auto.bpmn20.xml` があれば **自動ロード**
- キーボードショートカット (Delete, Ctrl/Cmd+Z など) 標準サポート

## デモ

```
# クローン & 起動 (例: Python HTTP server)
$ git clone <this-repo-url>
$ cd <repo>
$ python -m http.server 8080
# ブラウザで http://localhost:8080/bpmn-js-editor.html を開く
```

静的ホスティング (GitHub Pages / Vercel / S3 等) に `bpmn-js-editor.html` を置くだけでも動きます。

## 使い方

| UI                  | 説明                                     |
| ------------------- | ---------------------------------------- |
| 📂 **ファイル選択** | `.bpmn` / `.xml` を読み込み              |
| ➕ **New Diagram**  | 空の BPMN 図を生成                       |
| 💾 **Save BPMN**    | 編集結果を `diagram.bpmn` でダウンロード |
| 🖼 **Save SVG**      | SVG 画像をダウンロード                   |

> TIP: `#canvas` にファイルをドラッグ & ドロップしても読み込めます。

## ファイル構成

```
├─ bpmn-js-editor.html   # メイン HTML (エディタ本体)
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

## 作者

森 宝松 / 合同会社 Kinova
