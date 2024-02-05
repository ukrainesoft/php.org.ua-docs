---
navigation:
  - function.ftp-mkdir.md: « ftp\_mkdir
  - function.ftp-nb-continue.md: ftp\_nb\_continue »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_mlsd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_mlsd

(PHP 7 >= 7.2.0, PHP 8)

ftp\_mlsd — Повертає список файлів у заданій директорії

### Опис

```methodsynopsis
ftp_mlsd(FTP\Connection $ftp, string $directory): array|false
```

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`directory`

Директорія, список файлів якої буде повернутий.

### Значення, що повертаються

Повертає масив масивів з інформацією про файли із зазначеної директорії у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_mlsd()\*\*\*\*

```php
<?php

// установить основное соединение
$ftp = ftp_connect($ftp_server);

// авторизоваться на сервере, используя имя пользователя и пароль
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получить содержимое текущей директории
$contents = ftp_mlsd($ftp, ".");

// вывод $contents
var_dump($contents);

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(5) {
  [0]=>
  array(8) {
    ["name"]=>
    string(1) "."
    ["modify"]=>
    string(14) "20171212154511"
    ["perm"]=>
    string(7) "flcdmpe"
    ["type"]=>
    string(4) "cdir"
    ["unique"]=>
    string(11) "811U5740002"
    ["UNIX.group"]=>
    string(2) "33"
    ["UNIX.mode"]=>
    string(4) "0755"
    ["UNIX.owner"]=>
    string(2) "33"
  }
  [1]=>
  array(8) {
    ["name"]=>
    string(2) ".."
    ["modify"]=>
    string(14) "20171212154511"
    ["perm"]=>
    string(7) "flcdmpe"
    ["type"]=>
    string(4) "pdir"
    ["unique"]=>
    string(11) "811U5740002"
    ["UNIX.group"]=>
    string(2) "33"
    ["UNIX.mode"]=>
    string(4) "0755"
    ["UNIX.owner"]=>
    string(2) "33"
  }
  [2]=>
  array(8) {
    ["name"]=>
    string(11) "public_html"
    ["modify"]=>
    string(14) "20171211171525"
    ["perm"]=>
    string(7) "flcdmpe"
    ["type"]=>
    string(3) "dir"
    ["unique"]=>
    string(11) "811U5740525"
    ["UNIX.group"]=>
    string(2) "33"
    ["UNIX.mode"]=>
    string(4) "0755"
    ["UNIX.owner"]=>
    string(2) "33"
  }
  [3]=>
  array(8) {
    ["name"]=>
    string(10) "public_ftp"
    ["modify"]=>
    string(14) "20171211174536"
    ["perm"]=>
    string(7) "flcdmpe"
    ["type"]=>
    string(3) "dir"
    ["unique"]=>
    string(11) "811U57405EE"
    ["UNIX.group"]=>
    string(2) "33"
    ["UNIX.mode"]=>
    string(4) "0755"
    ["UNIX.owner"]=>
    string(2) "33"
  }
  [4]=>
  array(8) {
    ["name"]=>
    string(3) "www"
    ["modify"]=>
    string(14) "www"
    ["perm"]=>
    string(7) "flcdmpe"
    ["type"]=>
    string(3) "dir"
    ["unique"]=>
    string(11) "811U5740780"
    ["UNIX.group"]=>
    string(2) "33"
    ["UNIX.mode"]=>
    string(4) "0755"
    ["UNIX.owner"]=>
    string(2) "33"
  }
}
```

### Дивіться також

-   [ftp\_rawlist()](function.ftp-rawlist.md) \- Повертає докладний список файлів у заданій директорії
-   [ftp\_nlist()](function.ftp-nlist.md) \- Повертає список файлів у заданій директорії
