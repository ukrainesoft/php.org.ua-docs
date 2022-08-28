Повертає час останньої модифікації файлу

-   [« ftp\_login](function.ftp-login.html)
    
-   [ftp\_mkdir »](function.ftp-mkdir.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Повертає час останньої модифікації файлу
    

# ftpmdtm

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpmdtm — Повертає час останньої модифікації файлу

### Опис

```methodsynopsis
ftp_mdtm(FTP\Connection $ftp, string $filename): int
```

**ftpmdtm()** повертає час останньої модифікації віддаленого файлу.

> **Зауваження**
> 
> Не всі сервери підтримують цю функцію!

> **Зауваження**
> 
> **ftpmdtm()** не працює із директоріями.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`filename`

Файл, час модифікації якого потрібно отримати.

### Значення, що повертаються

Повертає час останньої модифікації у вигляді *локальною* тимчасової мітки Unix або -1 у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpmdtm()****

```php
<?php

$file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

//  получение времени модификации файла
$buff = ftp_mdtm($ftp, $file);

if ($buff != -1) {
    // дата последней модификации somefile.txt : March 26 2003 14:16:41.
    echo "Дата последней модификации $file : " . date("F d Y H:i:s.", $buff);
} else {
    echo "Не удалось выполнить mdtime";
}

// закрытие соединения
ftp_close($ftp);

?>
```