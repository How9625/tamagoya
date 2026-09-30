# 島らっきょう レシピ・見積もり・発注 統合版

## ファイル構成
- index.html：紹介・レシピ・購入案内
- order.html：元の発注サイトの価格計算・注文送信
- prep.html：下処理ガイド
- style.css：下処理ページのデザイン
- control.html：価格設定を作る管理用ページ
- settings.json：現在の基準価格と既存の注文送信先
- CNAME：shimarakkyo-order.shop

## GitHubへの配置
ZIPを解凍し、このフォルダー内の7ファイルを既存の shimarakkyo-order リポジトリのトップ階層に配置・上書きします。
フォルダーごと入れるのではなく、index.html、order.htmlなどが同じ階層に並ぶようにしてください。
新しいindex.htmlはレシピページです。以前のindex.htmlの発注機能はorder.htmlにあります。
既存のGitHub Pages公開設定はそのまま使用してください。

## ページのURL
- https://shimarakkyo-order.shop/ ：レシピ
- https://shimarakkyo-order.shop/order.html ：見積もり・発注
- https://shimarakkyo-order.shop/prep.html ：下処理
- https://shimarakkyo-order.shop/control.html ：価格設定

カスタムドメインのDNS設定は別途必要です。このファイルのアップロードだけではDNS設定は変更されません。
従来の発注URLのトップページはレシピに変わります。直接発注ページへ案内する際は /order.html を使用してください。

## 価格の変更
control.htmlを開き、生成されたJSON全文をsettings.jsonに貼り付けて更新します。
注文送信先gasUrlは保持されます。現在の800g基準価格は3,800円です。

## 引き継いだ機能
元の重量選択、皮付き・皮なし、割引、発送予定、通常配送の注文送信、BASEへの案内を保持しています。
BASEリンクは元の https://tamagoya.base.ec/ です。

## 確認範囲
ファイル間リンク、JavaScript構文、元の価格計算・注文送信コードの保持を確認しています。
実際の注文送信やGitHubへのアップロードは行っていません。公開後は通常配送の見積もりとBASEリンクをご確認ください。
