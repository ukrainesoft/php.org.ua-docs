Завантажує файл на FTP-сервер

-   [« ftppasv](function.ftp-pasv.html)
    
-   [ftppwd »](function.ftp-pwd.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Завантажує файл на FTP-сервер
    

# ftpput

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpput — Завантажує файл на сервер FTP

### Опис

```methodsynopsis
ftp_put(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftpput()** завантажує локальний файл на сервер FTP.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`remote_filename`

Шлях до файлу на сервері FTP.

`local_filename`

Шлях до локального файлу.

`mode`

Визначає режим передачі. Може приймати значення **`FTP_ASCII`** або **`FTP_BINARY`**

`offset`

Задає позицію у віддаленому файлі, в яку розпочнеться завантаження

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|        | Тепер параметр `mode` опціональний. Раніше він був обов'язковим.                                                                                  |

### Приклади

**Приклад #1 Приклад використання **ftpput()****

```php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// загрузка файла
if (ftp_put($ftp, $remote_file, $file, FTP_ASCII)) {
 echo "$file успешно загружен на сервер\n";
} else {
 echo "Не удалось загрузить $file на сервер\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftppasv()](function.ftp-pasv.html) - Вмикає або вимикає пасивний режим
-   [ftpfput()](function.ftp-fput.html) - Завантажує попередньо відкритий файл на FTP-сервер
-   [ftpнбfput()](function.ftp-nb-fput.html) - Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі
-   [ftpнбput()](function.ftp-nb-put.html) - Завантажує файл на сервер FTP в асинхронному режимі