---
navigation:
  - function.ftp-login.md: « ftp\_login
  - function.ftp-mkdir.md: ftp\_mkdir »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_mdtm
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_mdtm

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_mdtm — Повертає час останньої модифікації файлу

### Опис

```methodsynopsis
ftp_mdtm(FTP\Connection $ftp, string $filename): int
```

**ftp\_mdtm()** повертає час останньої модифікації віддаленого файлу.

> **Зауваження** :
> 
> Не всі сервери підтримують цю функцію!

> **Зауваження** :
> 
> **ftp\_mdtm()** не працює із директоріями.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`filename`

Файл, час модифікації якого потрібно отримати.

### Значення, що повертаються

Повертає час останньої модифікації у вигляді *локальною* тимчасової мітки Unix або -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_mdtm()\*\*\*\*

```php
<?php

$file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

//  получение времени модификации файла
$buff = ftp_mdtm($ftp, $file);

if ($buff != -1) {
    // дата последней модификации somefile.txt : March 26 2003 14:16:41.
    echo "Дата последней модификации $file : " . date("F d Y H:i:s.", $buff);
} else {
    echo "Не удалось выполнить mdtime";
}

// закрытие соединения
ftp_close($ftp);

?>
```
