---
navigation:
  - function.ftp-site.md: « ftp\_site
  - function.ftp-ssl-connect.md: ftp\_ssl\_connect »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_size

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_size — Повертає розмір вказаного файлу

### Опис

```methodsynopsis
ftp_size(FTP\Connection $ftp, string $filename): int
```

**ftp\_size()** повертає розмір заданого файлу у байтах.

> **Зауваження** :
> 
> Не всі сервери FTP підтримують цю можливість.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`filename`

Ім'я файлу на сервері.

### Значення, що повертаються

Повертає розмір файлу або -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_size()\*\*\*\*

```php
<?php

$file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получение размера файла $file
$res = ftp_size($ftp, $file);

if ($res != -1) {
    echo "Размер файла $file: $res байт";
} else {
    echo "Не удалось определить размер файла $file";
}

// закрытие соединения
ftp_close($ftp);

?>
```

### Дивіться також

-   [ftp\_rawlist()](function.ftp-rawlist.md) \- Повертає докладний список файлів у заданій директорії
