---
navigation:
  - function.ftp-quit.md: « ftp\_quit
  - function.ftp-rawlist.md: ftp\_rawlist »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_raw
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_raw

(PHP 5, PHP 7, PHP 8)

ftp\_raw — Надсилає довільну команду FTP-серверу

### Опис

```methodsynopsis
ftp_raw(FTP\Connection $ftp, string $command): ?array
```

Отправляет произвольную команду`command` FTP-сервер.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`command`

Команда.

### Значення, що повертаються

Повертає відповідь сервера у вигляді масиву рядків або **`null`**в случае возникновения ошибки. Функция**ftp\_raw()** не інтерпретує відповідь сервера та не визначає, чи успішно виконано команду.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Использование**ftp\_raw()**для входа на FTP-сервер**

```php
<?php
$ftp = ftp_connect("ftp.example.com");

/* То же самое, что:
   ftp_login($ftp, "joeblow", "secret"); */
ftp_raw($ftp, "USER joeblow");
ftp_raw($ftp, "PASS secret");
?>
```

### Дивіться також

-   [ftp\_exec()](function.ftp-exec.md) \- Запитує виконання команди на FTP-сервері
