---
layout: post.en
title: Groonga 4.0.9 users, please upgrade to Groonga 4.1.0
description: Groonga 4.0.9 users, please upgrade to Groonga 4.1.0
---

## Groonga 4.0.9 users, please upgrade to Groonga 4.1.0

Groonga 4.0.9 has a serious bug that may break
index. [Groonga 4.1.0 has been released](http://groonga.org/en/blog/2015/01/09/release.html).

The bug has effect to Mroonga users. If you're using Groonga 4.0.9,
please upgrade to Groonga 4.1.0.

If you installed Mroonga via package management system, please upgrade
Groonga as usual. Mroonga isn't upgraded bug Groonga will be upgraded
to 4.1.0. Because Groonga 4.1.0 packages are provided.

If you installed Mroonga from source code. You can only build and
install Groonga. You don't need to re-build and re-install Mroonga.

You should not forget to restart your MySQL/MariaDB after you upgrade
to Groonga 4.1.0. If you don't restart your MySQL/MariaDB, new Groonga
isn't used. You can confirm that Groonga 4.1.0 is used from your
Mroonga via `mroonga_libgroonga_version` variable. すればわかります。

If you get "4.0.9" like the following, Groonga 4.0.9 is used. Please
upgrade to Groonga 4.1.0:

    mysql> SHOW VARIABLES LIKE "mroonga_libgroonga_version";
    +----------------------------+-------+
    | Variable_name              | Value |
    +----------------------------+-------+
    | mroonga_libgroonga_version | 4.0.9 |
    +----------------------------+-------+
    1 row in set (0.00 sec)

If you get "4.1.0" like the following, you've upgraded to Groonga
4.1.0 successfully:

    mysql> SHOW VARIABLES LIKE "mroonga_libgroonga_version";
    +----------------------------+-------+
    | Variable_name              | Value |
    +----------------------------+-------+
    | mroonga_libgroonga_version | 4.1.0 |
    +----------------------------+-------+
    1 row in set (0.00 sec)

Please re-create your all indexes after you confirm Groonga 4.1.0 is
used. You can re-created a index by the following SQLs:

    mysql> ALTER TABLE ${TABLE_NAME} DISABLE KEYS;
    mysql> ALTER TABLE ${TABLE_NAME} ENABLE KEYS;

If you didn't change your indexes by Groonga 4.0.9, you don't need to
re-create your indexes. "change" means "add", "remove" and
"update". If you use your indexes only for "search" by Groonga 4.0.9,
you don't need to re-create your indexes.

If you know more information or have any question, please ask it on
[the mailing list](http://sourceforge.net/p/groonga/mailman/groonga-talk/)
or [@groonga](https://twitter.com/groonga). We'll answer it.

We're sorry for your inconvenient. 4.0.9 users, please upgrade your
Groonga.
