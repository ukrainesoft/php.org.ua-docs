---
navigation:
  - function.ftp-put.html: « ftpput
  - function.ftp-quit.html: ftpquit »
  - index.html: PHP Manual
  - ref.ftp.html: Функції FTP
title: ftppwd
---
# ftppwd

(PHP 4, PHP 5, PHP 7, PHP 8)

ftppwd — Повертає ім'я поточної директорії

### Опис

```methodsynopsis
ftp_pwd(FTP\Connection $ftp): string|false
```

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає ім'я поточної директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftppwd()****

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// смена текущей директории на public_html
ftp_chdir($ftp, 'public_html');

// вывод имени текущей директории
echo ftp_pwd($ftp); // /public_html

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftpchdir()](function.ftp-chdir.html) - Змінює поточну директорію на FTP-сервері
-   [ftpcdup()](function.ftp-cdup.html) - Переходить до батьківської директорії
