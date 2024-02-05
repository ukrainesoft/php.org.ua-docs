---
navigation:
  - install.pecl.php-config.md: « php-config
  - install.problems.md: Проблеми? »
  - index.md: PHP Manual
  - install.pecl.md: Встановлення модулів PECL
title: Компіляція модулів PECL статично в PHP
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Компіляція модулів PECL статично в PHP

Можливо, потрібно зібрати модуль PECL статично в бінарний файл PHP. Для цього необхідно помістити код модуля в директорію /path/to/php/src/dir/ext/ та викликати перегенерацію конфігураційних скриптів через систему збирання PHP.

```
$ cd /path/to/php/src/dir/ext
$ pecl download extname
$ gzip -d < extname.tgz | tar -xvf -
$ mv extname-x.x.x extname
```

У результаті буде створено таку директорію:

/path/to/php/src/dir/ext/extname

Після цього PHP необхідно заново перезбирати конфігураційний скрипт, після чого він може бути зібраний як завжди:

$ cd /path/to/php/src/dir  
$ rm configure  
$ ./buildconf --force  
$ ./configure --help  
$ ./configure --with-extname --enable-someotherext --with-foobar  
$ make  
$ make install

> **Зауваження**: Для запуска скрипта**buildconf**понадобится команда**autoconf** версії `2.68`и команда**automake** версії `1.4+` (новіші версії скрипту **autoconf** можуть працювати, але не підтримуються).

В зависимости от модуля будет использован один из двух параметров —**\--enable-extname** або **\--with-extname**. Зазвичай модуль, який не потребує зовнішніх бібліотек, використовує параметр **\--enable**. Щоб переконатися в цьому, можна виконати команду **buildconf** :

$ ./configure --help | grep extname
