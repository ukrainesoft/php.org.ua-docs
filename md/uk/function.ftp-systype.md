Повертає тип операційної системи FTP-сервера

-   [« ftpsslconnect](function.ftp-ssl-connect.html)
    
-   [FTPConnection »](class.ftp-connection.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
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

Ан [FTPConnection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає тип операційної системи FTP-сервера або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

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