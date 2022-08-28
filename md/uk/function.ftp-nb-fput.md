Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі

-   [« ftp\_nb\_fget](function.ftp-nb-fget.html)
    
-   [ftp\_nb\_get »](function.ftp-nb-get.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі
    

# ftpнбfput

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpнбfput — Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі

### Опис

```methodsynopsis
ftp_nb_fput(    FTP\Connection $ftp,    string $remote_filename,    resource $stream,    int $mode = FTP_BINARY,    int $offset = 0): int
```

**ftpнбfput()** закачує дані з дескриптора файлу до віддаленого файлу на FTP-сервері.

Різниця між цією функцією та [ftp\_fput()](function.ftp-fput.html) полягає в тому, що ця функція завантажує файл асинхронно, тому ваша програма може здійснювати інші операції, поки файл закачується.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`remote_filename`

Шлях до віддаленого файлу.

`stream`

Відкритий файловий дескриптор локального файлу. Читання припиняється при досягненні кінця файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, або **`FTP_BINARY`**

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Описание                                                                                                                                              |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|        | Тепер параметр `mode` опціональний. Раніше він був обов'язковим.                                                                                      |

### Приклади

**Приклад #1 Приклад використання **ftpнбfput()****

```php
<?php

$file = 'index.php';

$fp = fopen($file, 'r');

$ftp = ftp_connect($ftp_server);

$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// Начало загрузки
$ret = ftp_nb_fput($ftp, $file, $fp, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // производим какие-то действия ...
   echo ".";

   // продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}

fclose($fp);
?>
```

### Дивіться також

-   [ftp\_nb\_put()](function.ftp-nb-put.html) - Завантажує файл на сервер FTP в асинхронному режимі
-   [ftp\_nb\_continue()](function.ftp-nb-continue.html) - Продовжує асинхронну операцію
-   [ftp\_put()](function.ftp-put.html) - Завантажує файл на FTP-сервер
-   [ftp\_fput()](function.ftp-fput.html) - Завантажує попередньо відкритий файл на FTP-сервер