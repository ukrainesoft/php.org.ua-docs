---
navigation:
  - function.ftp-ssl-connect.md: « ftp\_ssl\_connect
  - class.ftp-connection.md: FTP\\Connection »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_systype
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_systype

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_systype — Повертає тип операційної системи сервера FTP

### Опис

```methodsynopsis
ftp_systype(FTP\Connection $ftp): string|false
```

Повертає тип операційної системи сервера FTP.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

### Значення, що повертаються

Повертає тип операційної системи FTP-сервера або \*\*`false`\*\*при возникновении ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_systype()\*\*\*\*

```php
<?php

// установка соединения
$ftp = ftp_connect('ftp.example.com');
ftp_login($ftp, 'user', 'password');

// получение типа системы
if ($type = ftp_systype($ftp)) {
    echo "example.com использует $type\n";
} else {
    echo "Не удалось определить тип системы";
}

?>
```

Висновок наведеного прикладу буде схожим на:

```
example.com использует UNIX
```
