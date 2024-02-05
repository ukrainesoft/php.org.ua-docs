---
navigation:
  - function.ftp-chmod.md: « ftp\_chmod
  - function.ftp-connect.md: ftp\_connect »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_close

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ftp\_close — Закриває з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_close(FTP\Connection $ftp): bool
```

**ftp\_close()** закриває вказаний ідентифікатор з'єднання із сервером та звільняє resource.

> **Зауваження** :
> 
> Після виклику цієї функції, з'єднання більше не може бути використане, і при необхідності має бути встановлене заново за допомогою функції [ftp\_connect()](function.ftp-connect.md)

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_close()\*\*\*\*

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// вывод текущей директории
echo ftp_pwd($ftp); // /

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_connect()](function.ftp-connect.md) \- Встановлює з'єднання з FTP-сервером
