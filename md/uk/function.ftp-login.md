Виконує вхід на FTP-сервер

-   [« ftp\_get](function.ftp-get.html)
    
-   [ftp\_mdtm »](function.ftp-mdtm.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Виконує вхід на FTP-сервер
    

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

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`username`

Ім'я користувача (`USER`

`password`

Пароль (`PASS`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо увійти на сервер не вдалося, PHP виведе попередження.

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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