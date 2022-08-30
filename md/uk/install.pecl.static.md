Компіляція модулів PECL статично в PHP

-   [« php-config](install.pecl.php-config.html)
    
-   [Проблеми? »](install.problems.md)
    
-   [PHP Manual](index.md)
    
-   [Установка модулей PECL](install.pecl.md)
    
-   Компіляція модулів PECL статично в PHP
    

## Компіляція модулів PECL статично в PHP

Можливо, ви захочете зібрати модуль PECL статично у ваш бінарний файл PHP. Для цього необхідно помістити код модуля в директорію php-src/ext/ та викликати перегенерацію конфігураційних скриптів через систему збирання PHP.

```
$ cd /your/phpsrcdir/ext
$ pecl download extname
$ gzip -d < extname.tgz | tar -xvf -
$ mv extname-x.x.x extname
```

У результаті буде створено таку директорію:

/your/phpsrcdir/ext/extname

Після цього, виконайте заново складання конфігураційного скрипта PHP і потім зберіть PHP як завжди:

$ cd /your/phpsrcdir  
$rm configure  
$ ./buildconf --force  
$ ./configure --help  
$ ./configure --with-extname --enable-someotherext --with-foobar  
$ make  
$ make install

> **Зауваження**: Для запуску 'buildconf' скрипту вам знадобиться autoconf версії 2.13 та automake версії 1.4+ (новіші версії autoconf можуть працювати, але це не підтримується).

Залежно від модуля використовуватиметься одна з двох опцій `--enable-extname` або `--with-extname` . Зазвичай, якщо модуль не вимагає підключення зовнішніх бібліотек, використовується `--enable`. Щоб дізнатися про це, виконайте наступну команду після buildconf:

$./configure --help | grep extname