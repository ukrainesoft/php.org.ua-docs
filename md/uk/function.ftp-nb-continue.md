---
navigation:
  - function.ftp-mlsd.md: « ftpmlsd
  - function.ftp-nb-fget.md: ftpнбfget »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpнбcontinue
---
# ftpнбcontinue

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpнбcontinue — Продовжує асинхронну операцію

### Опис

```methodsynopsis
ftp_nb_continue(FTP\Connection $ftp): int
```

Продовжує надсилання або отримання файлу в асинхронному режимі.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpнбcontinue()****

```php
<?php

// Начало скачивания
$ret = ftp_nb_get($ftp, "test", "README", FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // Продолжение скачивания  ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}
?>
```
