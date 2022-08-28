Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі

-   [« ftp\_nb\_continue](function.ftp-nb-continue.html)
    
-   [ftp\_nb\_fput »](function.ftp-nb-fput.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі
    

# ftpнбfget

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpнбfget — Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі

### Опис

```methodsynopsis
ftp_nb_fget(    FTP\Connection $ftp,    resource $stream,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): int
```

**ftpнбfget()** завантажує віддалений файл із FTP-сервера.

Різниця між цією функцією та [ftp\_fget()](function.ftp-fget.html) полягає в тому, що ця функція отримує файл асинхронно, так що ваша програма може здійснювати інші операції, поки файл завантажується.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`stream`

Відкритий файловий дескриптор для збереження даних.

`remote_filename`

Шлях до віддаленого файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, або **`FTP_BINARY`**

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |
|  | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання **ftpнбfget()****

```php
<?php

// открыть файл для записи
$file = 'index.php';
$fp = fopen($file, 'w');

$ftp = ftp_connect($ftp_server);

$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// Начало скачивания
$ret = ftp_nb_fget($ftp, $fp, $file, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // производим какие-то действия ...
   echo ".";

   // продолжение скачивания ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}

// закрытие файла
fclose($fp);
?>
```

### Дивіться також

-   [ftp\_nb\_get()](function.ftp-nb-get.html) - Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
-   [ftp\_nb\_continue()](function.ftp-nb-continue.html) - Продовжує асинхронну операцію
-   [ftp\_fget()](function.ftp-fget.html) - Завантажує файл з FTP-сервера та зберігає його у попередньо відкритому файлі
-   [ftp\_get()](function.ftp-get.html) - Завантажує файл із FTP-сервера