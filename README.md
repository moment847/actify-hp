# Actify ホームページ

公開URL: https://actify.moment-tokyo.jp/

2026-10-06に提供されたActify-local.zipのindex.htmlとactify-guide.pdfを配置。
画像・フォント・CSS・JavaScriptはHTML内に含まれます。ビルド、依存パッケージ、環境変数は不要です。

## 公開構成

既存のCloudflare PagesとGitHub連携を維持します。本番ブランチはmain、ビルドコマンドは空欄、出力ディレクトリは「.」です。
PDFはindex.htmlと同じ階層に配置してください。送信フォームはなく、サービス資料PDFへのリンクがあります。

## 検証

1440・768・390・320px幅で横はみ出し、ページ内リンク、全画像、JavaScriptエラーを確認。スマホメニューとFAQの開閉も確認済み。資料PDFは15ページです。

## 復元

差し替え前のコミット: 7540fa7837592620dd3d8b0fb7f0f30594c926f5
問題があれば今回の差し替えコミットをrevertしてmainへ反映してください。
