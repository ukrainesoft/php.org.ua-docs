---
navigation:
  - function.ftp-get.md: « ftpget
  - function.ftp-mdtm.md: ftpmdtm »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftplogin
---
# ftplogin

(PHP 4, PHP 5, PHP 7, PHP 8)

ftplogin — Вхід на FTP-сервер

### Опис

```methodsynopsis
ftp_login(FTP\Connection $ftp, string $username, string $password): bool
```

Виконує вхід на сервер FTP.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`username`

Ім'я користувача (`USER`

`password`

Пароль (`PASS`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо увійти на сервер не вдалося, PHP виведе попередження.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftplogin()****

```php
<?php

$ftp_server = "ftp.example.com";
$ftp_user = "foo";
$ftp_pass = "bar";

// установить соединение или выйти
$ftp = ftp_connect($ftp_server) or die("Не удалось установить соединение с $ftp_server");

// попытка входа
if (@ftp_login($ftp, $ftp_user, $ftp_pass)) {
    echo "Произведён вход на $ftp_server под именем $ftp_user\n";
} else {
    echo "Не удалось войти под именем $ftp_user\n";
}

// закрыть соединение
ftp_close($ftp);
?>
```
