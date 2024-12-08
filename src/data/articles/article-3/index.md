---
title: "FigmaでVariablesを使って文字数ごとの見た目の違いを素早く検証する"
coverImage: "https://qiita-user-contents.imgix.net/https%3A%2F%2Fqiita-user-contents.imgix.net%2Fhttps%253A%252F%252Fcdn.qiita.com%252Fassets%252Fpublic%252Fadvent-calendar-ogp-background-7940cd1c8db80a7ec40711d90f43539e.jpg%3Fixlib%3Drb-4.0.0%26w%3D1200%26blend64%3DaHR0cHM6Ly9xaWl0YS11c2VyLXByb2ZpbGUtaW1hZ2VzLmltZ2l4Lm5ldC9odHRwcyUzQSUyRiUyRnFpaXRhLWltYWdlLXN0b3JlLnMzLmFwLW5vcnRoZWFzdC0xLmFtYXpvbmF3cy5jb20lMkYwJTJGMjE0Njc3JTJGcHJvZmlsZS1pbWFnZXMlMkYxNjk0NTkyNDA1P2l4bGliPXJiLTQuMC4wJmFyPTElM0ExJmZpdD1jcm9wJm1hc2s9ZWxsaXBzZSZmbT1wbmczMiZzPWUyZWUzYzU5YWI3YmU2YTNhNzdhN2RhNTg1YWJlN2Jk%26blend-x%3D120%26blend-y%3D467%26blend-w%3D82%26blend-h%3D82%26blend-mode%3Dnormal%26s%3D49d8fc9abe50dfa62c67b9caa2ba8b5c?ixlib=rb-4.0.0&w=1200&fm=jpg&mark64=aHR0cHM6Ly9xaWl0YS11c2VyLWNvbnRlbnRzLmltZ2l4Lm5ldC9-dGV4dD9peGxpYj1yYi00LjAuMCZ3PTk2MCZoPTMyNCZ0eHQ9RmlnbWElRTMlODElQTdWYXJpYWJsZXMlRTMlODIlOTIlRTQlQkQlQkYlRTMlODElQTMlRTMlODElQTYlRTYlOTYlODclRTUlQUQlOTclRTYlOTUlQjAlRTMlODElOTQlRTMlODElQTglRTMlODElQUUlRTglQTYlOEIlRTMlODElOUYlRTclOUIlQUUlRTMlODElQUUlRTklODElOTUlRTMlODElODQlRTMlODIlOTIlRTclQjQlQTAlRTYlOTclQTklRTMlODElOEYlRTYlQTQlOUMlRTglQTglQkMlRTMlODElOTklRTMlODIlOEImdHh0LWFsaWduPWxlZnQlMkN0b3AmdHh0LWNvbG9yPSUyMzNBM0MzQyZ0eHQtZm9udD1IaXJhZ2lubyUyMFNhbnMlMjBXNiZ0eHQtc2l6ZT01NiZ0eHQtcGFkPTAmcz1kN2VlOTcwMGU3MGYyODQ4ODQyZjYyY2U4ZTExN2Q2YQ&mark-x=120&mark-y=112&blend64=aHR0cHM6Ly9xaWl0YS11c2VyLWNvbnRlbnRzLmltZ2l4Lm5ldC9-dGV4dD9peGxpYj1yYi00LjAuMCZ3PTgzOCZoPTU4JnR4dD0lNDB4cnhveGN4b3gmdHh0LWNvbG9yPSUyMzNBM0MzQyZ0eHQtZm9udD1IaXJhZ2lubyUyMFNhbnMlMjBXNiZ0eHQtc2l6ZT0zNiZ0eHQtcGFkPTAmcz1mMzhlMDNlODEyZjRjNjYxNjRhMzFmYmU5MmIwYWZmYw&blend-x=242&blend-y=480&blend-w=838&blend-h=46&blend-fit=crop&blend-crop=left%2Cbottom&blend-mode=normal&s=882df3d220d247cd93ebb8fc81ab6184"
---

## この記事の概要

UI Stackのような概念が当たり前になりつつある今、Figmaでモックアップを作る際も「ちょうど良い文字数での表示」だけを検証することは少ないと思います。

短いものから長いものまで、色々なパターンを検証するでしょう。

ただ、その際に毎回ダミーテキストを考えるのも面倒です。

というわけで、Variablesを使ってあらかじめダミーテキストを定義しておき、時短を図るための記事です。

## 今回作るもの

見本として、以下の2つのコンポーネントを作成します。

| UserInfo | ArticleCard |
| --- | --- |
| ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/8b98bb84-94bb-1fb3-63d2-c580d529a4d3.png) | ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/4d5dd8ba-7b0c-c467-b8ab-b73f34cd9763.png) |
| ユーザーアイコン + ユーザー名を表示する | 記事タイトル + ユーザー情報 + 投稿日を表示する |

ArticleCardの中でUserInfoを使用しています。

## Variablesの設定

このようなVariablesを登録します。

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/fec83a8f-8e64-9706-fbbd-a37f5853848f.png)

* Collectionを別途作成する
    * 今回は`Dummy text`という名前で作成
    * 他のデザイントークンとは役割も必要なModeも違うので、別のCollectionにしておいた方が良い
* Modeを登録する
    * 今回はPlaceholder, Short, Medium, Longの4つ
    * ProfessionalとOrganizationプランはMode数が4つという制限があるので、このあたりがちょうど良いバランスと思われる
    * 空文字列もあり得る場合、Shortに半角スペースを入れるのも良さそう
* Variableを登録する
    * 今回は具体的な役割のテキストを登録している
    * 汎用的なダミーテキストを用意しておいて、Modeをデータベースの文字数制限に揃える（31文字, 255文字など）と揃えておくのも良い

## Componentsの作成

通常通りComponentを作成した上で、PropertyにVariableを適用するだけです。

1つ目のModeをPlaceholderにしておくことで、Variableの選択時や単にコンポーネントを配置したときに、そのテキストの意味が分かりやすくなります。

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/d0d4457f-9914-4bda-71e4-592170e39bac.png)

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/da0731cc-dee5-613b-4125-73e36f4495ba.png)

## ダミーテキストの検証

Componentを配置しているFrame、もしくは1つ1つのComponentを選び、AppearanceからVariableのModeを選択します。

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/64bb3465-727b-cc0a-e9c1-fd254db23254.png)

このように選ぶだけで、Variableを適用している箇所の見た目が変わります。
ネストされたComponent（ここではUserInfo）の中身も問題なく変化します。

![](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/ac836ed4-0e6b-c73b-d909-45f044d8df03.png)

これらを実施すると、このようなパターン違いの検証をすぐにできるようになります。
「記事一覧」のようなページであれば、ArticleCardコンポーネントを20個くらい並べて親FrameのAppearanceを切り替えることで一気に色々な場合の見た目を見れます。

| 種別 | 画像 |
| --- | --- |
| プレースホルダー状態での表示 | ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/e89572c6-748b-b8fc-2ad7-57b64296dbb8.png) |
| 短いテキスト | ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/f5f96431-878a-9dae-b1cc-45cb7d4fbcfc.png) |
| ちょうど良いテキスト | ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/a60d7c9a-df82-fa6d-f550-dd61bf8fb682.png) |
| 長いテキスト | ![image.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/214677/28714ae1-77e6-32e9-1494-9fd2355f0ffb.png) |

## 注意点

この手法をとった場合、決まったテキストではなく好きなテキストを流し込みたい場合はVariableをdetachしないといけません。

ただ、今回の記事カードのコンポーネントのように「具体的なテキストが必要なわけでも本番データと同期したいわけでもなく、Figmaデータとしてはすべてダミーテキストで構わない」というものもあると思います。
そういう場合はdetachする必要もないので、特にデメリットになることもないかと思います。

常にこのテクニックを使うというよりは、都度テキストを変える必要がある要素は都度変えて、すべてダミーテキストでも構わないようなものならこのテクニックを使う、と場合わけできると良いと思います。
