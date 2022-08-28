Продовжує асинхронну операцію

-   [« ftp\_mlsd](function.ftp-mlsd.html)
    
-   [ftp\_nb\_fget »](function.ftp-nb-fget.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Продовжує асинхронну операцію
    

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

Ан [FTP\\Connection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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