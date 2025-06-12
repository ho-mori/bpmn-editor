# 操作方法

このドキュメントでは、同梱の `index.html` を用いて BPMN ファイルを作成・編集する手順を説明します。

## 起動方法
1. リポジトリをクローン後、任意の HTTP サーバーで公開します。
   例:
   ```bash
   $ python -m http.server 8080
   ```
2. ブラウザで `http://localhost:8080/index.html` を開きます。

## 既存 BPMN の読み込み
- **ファイル選択** ボタンから `.bpmn` / `.xml` ファイルを指定します。
- あるいは `#canvas` 領域へファイルをドラッグ&ドロップします。
- リポジトリ直下に `allocation-auto.bpmn20.xml` が存在する場合、自動で読み込まれます。

## 新規作成
- **New Diagram** ボタンを押すと空の BPMN 図を生成します。

## 保存
- **Save BPMN** で編集結果を `diagram.bpmn` としてダウンロードします。
- **Save SVG** で BPMN 図のプレビュー画像 (SVG) をダウンロードします。

## 編集のポイント
- 要素はドラッグ&ドロップで追加できます。
- Delete キーで選択要素を削除できます。
- Ctrl/Cmd+Z でアンドゥ、Ctrl/Cmd+Shift+Z でリドゥできます。
