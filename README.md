# Actify ホームページ

https://actify.moment-tokyo.jp/ の静的サイトです。既存サイトから取得したHTMLを変更せずに移行しています。CSS・JavaScript・SVGは index.html に含まれます。Google Fontsのみ外部読み込みです。

## ローカル確認

```sh
python3 -m http.server 8001 --bind 127.0.0.1
```

ビルド・依存パッケージ・環境変数は不要です。お問い合わせは既存のLINEと電話リンクを利用します。

## Cloudflare Pages の GitHub 連携

同じ会社の moment-hp を管理しているCloudflareアカウントで操作します。

1. Workers & Pages から Pages の作成、既存Gitリポジトリのインポートを選択します（画面上の名称は変更される場合があります）。
2. GitHub の moment847/actify-hp を選択します。表示されなければCloudflareのGitHubアプリにこのリポジトリへのアクセスを追加します。
3. プロジェクト名: actify-hp（空いている場合）、本番ブランチ: main、フレームワーク: None、ビルドコマンド: 空欄、出力ディレクトリ: .、ルートディレクトリ: 既定値。
4. 公開後に発行される pages.dev のURLで、PC・スマートフォン表示、FAQ、スライダー、限界突破ボタン、LINE・電話リンクを確認します。
5. Pagesのカスタムドメインに actify.moment-tokyo.jp を登録します。既存DNSの actify レコードの種類・値・TTL・プロキシ状態を記録してから、Cloudflare画面の案内に従って対象レコードだけを切り替えます。
6. HTTPSで元のドメインを開き、Pagesのデプロイ内容と一致することを確認します。問題があれば記録した旧DNS設定へ戻します。

mainへのpushで自動公開されるのは、CloudflareのGitHub連携完了後です。親ドメイン・momentサイト・メール用MX/TXTなどのレコードは変更しません。旧ホスティングは切り替え検証が終わるまで保持します。

## 移行時点の既存事項

- 特定商取引法・プライバシーポリシーのリンクは元サイトで href="#" です。移行でも維持しており、リンク先ページの整備は別途必要です。
- 元サイトのdescription属性にはエスケープされていない引用符があります。完全一致での移行を優先してそのまま保持しています。
- robots.txt / sitemap.xml は元サイトで404でした。新規追加していません。
- 管理画面、フォーム送信処理、データベースはこのHTMLにはありません。
