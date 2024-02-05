---
navigation:
  - function.ftp-get.md: « ftp\_get
  - function.ftp-mdtm.md: ftp\_mdtm »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_login
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_login

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_login — Вхід на FTP-сервер

### Опис

```methodsynopsis
ftp_login(FTP\Connection $ftp, string $username, string $password): bool
```

Виконує вхід на сервер FTP.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`username`

Ім'я користувача (`USER`

`password`

Пароль (`PASS`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо увійти на сервер не вдалося, PHP виведе попередження.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_login()\*\*\*\*

```php
<?php

$ftp_server = "ftp.example.com";
$ftp_user = "foo";
$ftp_pass = "bar";

// установить соединение или выйти
$ftp = ftp_connect($ftp_server) or die("Не удалось установить соединение с $ftp_server");

// попытка входа
if (@ftp_login($ftp, $ftp_user, $ftp_pass)) {
    echo "Произведён вход на $ftp_server под именем $ftp_user\n";
} else {
    echo "Не удалось войти под именем $ftp_user\n";
}

// закрыть соединение
ftp_close($ftp);
?>
```
