Повертає розмір вказаного файлу

-   [« ftpsite](function.ftp-site.html)
    
-   [ftpsslconnect »](function.ftp-ssl-connect.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Повертає розмір вказаного файлу
    

# ftpsize

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpsize — Повертає розмір вказаного файлу

### Опис

```methodsynopsis
ftp_size(FTP\Connection $ftp, string $filename): int
```

**ftpsize()** повертає розмір заданого файлу у байтах.

> **Зауваження**
> 
> Не всі сервери FTP підтримують цю можливість.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`filename`

Ім'я файлу на сервері.

### Значення, що повертаються

Повертає розмір файлу або -1 у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpsize()****

```php
<?php

$file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получение размера файла $file
$res = ftp_size($ftp, $file);

if ($res != -1) {
    echo "Размер файла $file: $res байт";
} else {
    echo "Не удалось определить размер файла $file";
}

// закрытие соединения
ftp_close($ftp);

?>
```

### Дивіться також

-   [ftprawlist()](function.ftp-rawlist.html) - Повертає докладний список файлів у заданій директорії