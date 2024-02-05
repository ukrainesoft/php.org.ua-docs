---
navigation:
  - function.ftp-put.md: « ftp\_put
  - function.ftp-quit.md: ftp\_quit »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_pwd
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_pwd

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_pwd — Повертає ім'я поточної директорії

### Опис

```methodsynopsis
ftp_pwd(FTP\Connection $ftp): string|false
```

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

### Значення, що повертаються

Повертає ім'я поточної директорії або \*\*`false`\*\*при возникновении ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_pwd()\*\*\*\*

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

-   [ftp\_chdir()](function.ftp-chdir.md) \- Змінює поточну директорію на FTP-сервері
-   [ftp\_cdup()](function.ftp-cdup.md) \- Переходить до батьківської директорії
