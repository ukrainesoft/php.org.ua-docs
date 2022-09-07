---
navigation:
  - function.ftp-put.md: « ftpput
  - function.ftp-quit.md: ftpquit »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
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

Ан [FTPConnection](class.ftp-connection.md) instance.

### Значення, що повертаються

Повертає ім'я поточної директорії або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftppwd()****

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// смена текущей директории на public_html
ftp_chdir($ftp, 'public_html');

// вывод имени текущей директории
echo ftp_pwd($ftp); // /public_html

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftpchdir()](function.ftp-chdir.md) - Змінює поточну директорію на FTP-сервері
-   [ftpcdup()](function.ftp-cdup.md) - Переходить до батьківської директорії
