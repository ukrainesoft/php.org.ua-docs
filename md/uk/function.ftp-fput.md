Завантажує попередньо відкритий файл на сервер FTP

-   [« ftpfget](function.ftp-fget.html)
    
-   [ftpgetoption »](function.ftp-get-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функції FTP](ref.ftp.html)
    
-   Завантажує попередньо відкритий файл на сервер FTP
    

# ftpfput

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpfput — Завантажує попередньо відкритий файл на сервер FTP

### Опис

```methodsynopsis
ftp_fput(    FTP\Connection $ftp,    string $remote_filename,    resource $stream,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftpfput()** завантажує дані із файлового дескриптора у віддалений файл на FTP-сервері.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`remote_filename`

Шлях до віддаленого файлу.

`stream`

Відкритий файловий дескриптор локального файлу. Читання припиняється при досягненні кінця файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, або **`FTP_BINARY`**

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання **ftpfput()****

```php
<?php

// открыть файл для чтения
$file = 'somefile.txt';
$fp = fopen($file, 'r');

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка загрузки файла
if (ftp_fput($ftp, $file, $fp, FTP_ASCII)) {
    echo "Файл $file успешно загружен\n";
} else {
    echo "При загрузке $file произошла проблема\n";
}

// закрываем соединение и дескриптор файла
ftp_close($ftp);
fclose($fp);

?>
```

### Дивіться також

-   [ftpput()](function.ftp-put.html) - Завантажує файл на FTP-сервер
-   [ftpнбfput()](function.ftp-nb-fput.html) - Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі
-   [ftpнбput()](function.ftp-nb-put.html) - Завантажує файл на сервер FTP в асинхронному режимі