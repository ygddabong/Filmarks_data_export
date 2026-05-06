# Filmarks Review Exporter

Filmarksに記録した映画の評価・レビューを、ブラウザのコンソールからCSV形式でエクスポートするためのシンプルなスクリプトです。

## 概要

このスクリプトは、Filmarksのユーザーページから自分の映画データを取得し、CSVファイルとしてダウンロードします。

エクスポートできる内容は以下の通りです。

- 映画タイトル
- 評価
- レビュー本文
- Filmarksの作品ページURL

## 特徴

- ブラウザだけで実行可能
- 追加ライブラリ不要
- 複数ページを自動で取得
- CSV形式でダウンロード
- 日本語の文字化け対策としてBOM付きCSVを生成

## 注意事項

このスクリプトは、個人のバックアップやデータ移行を目的としています。

他のユーザーのデータを収集したり、Filmarksに過度なアクセスを行ったりする目的では使用しないでください。

また、このプロジェクトはFilmarks公式のものではありません。

## 使い方
1. [Filmarks](https://filmarks.com)にアクセスする
2. 自分のFilmarksユーザーページを開く
3. 開発者ツールを開く
   Chromeの場合は、以下の方法で開発者ツールを開けます。

```text
右クリック → 検証 → Console
```

ショートカットを使う場合:

```text
Mac: Command + Option + J
Windows: Ctrl + Shift + J
```

4. [スクリプト](https://github.com/ygddabong/Filmarks_data_export/blob/main/filmarks_data_export)を貼り付けて実行する

## スクリーンショット

### 自分のFilmarksユーザーページ
<img width="1920" height="1080" alt="스크린샷 2026-05-06 오후 10 36 10" src="https://github.com/user-attachments/assets/3ff943e2-6354-4b2f-8d43-62d80b64ed6d" />

### Console
<img width="1920" height="1080" alt="스크린샷 2026-05-06 오후 10 35 59" src="https://github.com/user-attachments/assets/a607c32e-5e11-4efc-a780-fb8ff28378dd" />

### Output
<img width="920" height="1045" alt="스크린샷 2026-05-06 오후 10 50 50" src="https://github.com/user-attachments/assets/9bf936cf-f773-4d9c-96d0-378fa336019a" />




## 出力形式

エクスポートされるCSVファイルには、以下のカラムが含まれます。

| カラム | 内容 |
|---|---|
| Title | 映画タイトル |
| Rating | 自分の評価 |
| Review | レビュー本文 |
| URL | Filmarksの作品ページURL |

出力例:

```csv
Title,Rating,Review,URL
"Drive My Car","4.2","素晴らしい映画だった。","https://filmarks.com/movies/..."
```

## 文字化けについて

CSVファイルをExcelで開いた際に日本語が文字化けしないように、スクリプトではBOMを追加しています。

もし文字化けが発生する場合は、Google SheetsやNumbersで開いてみてください。

## 動作しない場合

### エラーが表示される場合

自分のFilmarksユーザーページ上でスクリプトを実行しているか確認してください。

```text
https://filmarks.com/users/YOUR_USERNAME
```

### 途中で処理が止まる場合

ネットワークの状態やFilmarks側のページ読み込み状況によって、一時的に処理が止まる場合があります。

その場合は、少し時間を置いてから再度実行してください。

## 制限事項

このスクリプトはFilmarksのHTML構造に依存しています。

そのため、Filmarks側のデザインやクラス名が変更された場合、正しく動作しなくなる可能性があります。

また、非公開情報やログインしていないと見られない情報は取得できない場合があります。

## 免責事項

このプロジェクトはFilmarks公式のものではありません。

このスクリプトの使用は自己責任で行ってください。

個人利用の範囲で、自分自身のデータのバックアップや移行目的で使用してください。

Filmarksの利用規約やサーバー負荷に配慮し、過度なアクセスは行わないでください。

## License

MIT License
