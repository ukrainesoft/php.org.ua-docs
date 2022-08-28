Повертає тип операційної системи FTP-сервера

-   [« ftp\_ssl\_connect](function.ftp-ssl-connect.html)
    
-   [FTP\\Connection »](class.ftp-connection.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Повертає тип операційної системи FTP-сервера
    

# ftpsystype

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpsystype — Повертає тип операційної системи сервера FTP

### Опис

```methodsynopsis
ftp_systype(FTP\Connection $ftp): string|false
```

Повертає тип операційної системи сервера FTP.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає тип операційної системи FTP-сервера або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpsystype()****

```php
<?php

// установка соединения
$ftp = ftp_connect('ftp.example.com');
ftp_login($ftp, 'user', 'password');

// получение типа системы
if ($type = ftp_systype($ftp)) {
    echo "example.com использует $type\n";
} else {
    echo "Не удалось определить тип системы";
}

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
example.com использует UNIX
```