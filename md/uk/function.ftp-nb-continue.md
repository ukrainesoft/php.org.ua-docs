---
navigation:
  - function.ftp-mlsd.md: « ftp\_mlsd
  - function.ftp-nb-fget.md: ftp\_nb\_fget »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_nb\_continue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_nb\_continue

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ftp\_nb\_continue — Продовжує асинхронну операцію

### Опис

```methodsynopsis
ftp_nb_continue(FTP\Connection $ftp): int
```

Продовжує надсилання або отримання файлу в асинхронному режимі.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_nb\_continue()\*\*\*\*

```php
<?php

// Начало скачивания
$ret = ftp_nb_get($ftp, "test", "README", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Продолжение скачивания  ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}
?>
```
