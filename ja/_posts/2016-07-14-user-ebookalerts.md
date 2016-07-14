---
layout: post.ja
title: 事例紹介 - 電子書籍アラート
---

## 事例紹介 - 電子書籍アラート

[電子書籍アラート](https://ebookalerts.net/)というWebサービスでMroongaを使っているので紹介します。

> 「電子書籍アラート」はKindleの新刊情報・セール情報をRSSで配信するサービスです。対象書籍は2016年7月時点で約40万件あり、全文検索で絞り込めます。
>
> Mroongaの[ORDER BY LIMIT最適化](/ja/docs/reference/optimizations.html#order-by-limit)を活用しています。「ORDER BY LIMIT最適化」はヒット件数が増えても高速に先頭N件を取得できるようにするための高速化です。RSSは最新N件の情報だけを配信するフォーマットなので、先頭N件を取得する処理は重要な処理です。Mroongaがこの処理を高速に実行できるため非常に役に立っています。
>
> また、開発時に[チャットルーム](https://gitter.im/groonga/ja)で開発者と相談できたことはとても助かりました。気軽に質問したり改善要望を伝えたりできるからです。
>
> 高速に処理してくれる上にユーザーサポートも充実しているためMroongaを選んでよかったです。これからも別の機会のときにもMroongaを活用していきます。

Mroongaを利用している方で紹介してもよいという方はぜひgroonga at groonga.orgまでご連絡ください！
