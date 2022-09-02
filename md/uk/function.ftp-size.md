---
navigation:
  - function.ftp-site.md: « ftpsite
  - function.ftp-ssl-connect.md: ftpsslconnect »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpsize
---
# ftpsize

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpsize — Повертає розмір вказаного файлу

### Опис

```methodsynopsis
ftp_size(FTP\Connection $ftp, string $filename): int
```

**ftpsize()** повертає розмір заданого файлу у байтах.

> **Зауваження**
> 
> Не всі сервери FTP підтримують цю можливість.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`filename`

Ім'я файлу на сервері.

### Значення, що повертаються

Повертає розмір файлу або -1 у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpsize()****

```php
<?php

$file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получение размера файла $file
$res = ftp_size($ftp, $file);

if ($res != -1) {
    echo "Размер файла $file: $res байт";
} else {
    echo "Не удалось определить размер файла $file";
}

// закрытие соединения
ftp_close($ftp);

?>
```

### Дивіться також

-   [ftprawlist()](function.ftp-rawlist.md) - Повертає докладний список файлів у заданій директорії
