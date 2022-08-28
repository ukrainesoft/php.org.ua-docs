Завантажує файл із FTP-сервера

-   [« ftp\_get\_option](function.ftp-get-option.html)
    
-   [ftp\_login »](function.ftp-login.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Завантажує файл із FTP-сервера
    

# ftpget

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpget — Завантажує файл із FTP-сервера

### Опис

```methodsynopsis
ftp_get(    FTP\Connection $ftp,    string $local_filename,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftpget()** завантажує видалений файл з сервера FTP і зберігає його локально.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`local_filename`

Шлях до локального файлу (файл буде перезаписано, якщо існує).

`remote_filename`

Шлях до віддаленого файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, або **`FTP_BINARY`**

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Тепер параметр `mode` опціональний. Раніше він був обов'язковим.                                                                                      |

### Приклади

**Приклад #1 Приклад використання **ftpget()****

```php
<?php

// объявление переменных
$local_file = 'local.zip';
$server_file = 'server.zip';

// установка соединения
$conn_id = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// попытка скачать $server_file и сохранить в $local_file
if (ftp_get($conn_id, $local_file, $server_file, FTP_BINARY)) {
    echo "Произведена запись в $local_file\n";
} else {
    echo "Не удалось завершить операцию\n";
}

// закрытие соединения
ftp_close($conn_id);

?>
```

### Дивіться також

-   [ftp\_pasv()](function.ftp-pasv.html) - Вмикає або вимикає пасивний режим
-   [ftp\_fget()](function.ftp-fget.html) - Завантажує файл з FTP-сервера та зберігає його у попередньо відкритому файлі
-   [ftp\_nb\_get()](function.ftp-nb-get.html) - Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
-   [ftp\_nb\_fget()](function.ftp-nb-fget.html) - Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі