---
layout: post.ja
title: Groonga 4.0.9ユーザーは4.1.0へのアップグレードを推奨
description: Groonga 4.0.9ユーザーは4.1.0へのアップグレードを推奨します
---

## Groonga 4.0.9ユーザーは4.1.0へのアップグレードを推奨

Groonga 4.0.9に「インデックスが壊れる可能性がある」という問題が見つかり、[Groonga 4.1.0がリリース](http://groonga.org/ja/blog/2015/01/09/release.html)されました。

この問題はMroongaユーザーにも影響があります。もし、Groonga 4.0.9を使っている場合はGroonga 4.1.0にアップグレードしてください。

パッケージでインストールしている場合はパッケージ管理システムのいつも通りの方法でGroongaをアップグレードしてください。Mroongaは更新されませんが、Groonga 4.1.0のパッケージが提供されているのでGroongaがアップグレードされるはずです。

ソースコードからインストールしている場合はGroongaだけをアップグレードすればよいです。Mroongaをビルドし直す必要はありません。

Groongaをアップグレードした後はMySQL/MariaDBを再起動することを忘れないでください！再起動しないと新しいGroongaが使われません。Groonga 4.1.0が使われているかは`mroonga_libgroonga_version`変数を確認すればわかります。

次のように「4.0.9」と返ってきたらGroonga 4.0.9が使われています。Groonga 4.1.0にアップグレードしてください。

    mysql> SHOW VARIABLES LIKE "mroonga_libgroonga_version";
    +----------------------------+-------+
    | Variable_name              | Value |
    +----------------------------+-------+
    | mroonga_libgroonga_version | 4.0.9 |
    +----------------------------+-------+
    1 row in set (0.00 sec)

次のように「4.1.0」と返ってきたらGroonga 4.1.0へのアップグレードが完了しています。

    mysql> SHOW VARIABLES LIKE "mroonga_libgroonga_version";
    +----------------------------+-------+
    | Variable_name              | Value |
    +----------------------------+-------+
    | mroonga_libgroonga_version | 4.1.0 |
    +----------------------------+-------+
    1 row in set (0.00 sec)

Groonga 4.1.0が使われていることを確認したらインデックスを作りなおしてください。次のSQLでインデックスを作り直せます。

    mysql> ALTER TABLE ${テーブル名} DISABLE KEYS;
    mysql> ALTER TABLE ${テーブル名} ENABLE KEYS;

Groonga 4.0.9でインデックスを変更（追加・削除・変更）した場合はインデックスを作りなおしてください。インデックスが壊れている可能性があるためです。

Groonga 4.0.9でインデックスを変更せずに検索だけしていた場合はインデックスを作りなおす必要はありません。

以上の情報以外にも知りたいことがある方は[メーリングリスト](http://lists.sourceforge.jp/mailman/listinfo/groonga-dev)や[@groonga](https://twitter.com/groonga)経由で質問してください。回答します。

ご不便をお掛けして申し訳ありませんが、Groonga 4.0.9を使っている方は対応をお願いします。
