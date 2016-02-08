---
layout: post.ja
title: 「隔週連載groonga 第8回　CentOS6でのRPMパッケージを用いた MySQL 5.6 & mroonga & PHP 5.4 環境の作り方」公開
description: gihyo.jpさんで公開された記事「隔週連載groonga 第8回　CentOS6でのRPMパッケージを用いた MySQL 5.6 & mroonga & PHP 5.4 環境の作り方」の紹介
---
## 「隔週連載groonga 第8回　CentOS6でのRPMパッケージを用いた MySQL 5.6 & mroonga & PHP 5.4 環境の作り方」公開

[gihyo.jp](http://gihyo.jp/) さんで [Tritonn](http://qwik.jp/tritonn/)
からmroongaへの移行事例を紹介した記事が公開されています。

-   [隔週連載groonga 第6回　[実録]
    MySQL向け全文検索エンジン「Tritonn」から「mroonga」への移行ガイド（1）](http://gihyo.jp/dev/clip/01/groonga/0006)
-   [隔週連載groonga 第7回　[実録]
    MySQL向け全文検索エンジン「Tritonn」から「mroonga」への移行ガイド（2）](http://gihyo.jp/dev/clip/01/groonga/0007)

実際に [@yoshi_ken](https://twitter.com/yoshi_ken)
さんが実施した移行事例を元にしているので、とても実践的になっています。

今回紹介するのは、その移行作業で必要になったRPMパッケージングのノウハウを別記事としてまとめた、
[隔週連載groonga 第8回　CentOS6でのRPMパッケージを用いた MySQL 5.6 &
mroonga & PHP 5.4
環境の作り方](http://gihyo.jp/dev/clip/01/groonga/0008) です。

例えば、mroonga公式ではCentOS 6向けには標準であるMySQL
5.1系に依存したRPMパッケージしか提供していません。
MySQL
5.6系を使いたいなど独自の要求に合わせた構成をRPMパッケージで一式管理したいというときに非常に参考になるでしょう。
