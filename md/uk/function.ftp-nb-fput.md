---
navigation:
  - function.ftp-nb-fget.md: « ftp\_nb\_fget
  - function.ftp-nb-get.md: ftp\_nb\_get »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_nb\_fput
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_nb\_fput

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ftp\_nb\_fput — Завантажує попередньо відкритий файл на сервер FTP в асинхронному режимі

### Опис

```methodsynopsis
ftp_nb_fput(    FTP\Connection $ftp,    string $remote_filename,    resource $stream,    int $mode = FTP_BINARY,    int $offset = 0): int
```

**ftp\_nb\_fput()** закачує дані з дескриптора файлу до віддаленого файлу на FTP-сервері.

Різниця між цією функцією та [ftp\_fput()](function.ftp-fput.md) полягає в тому, що ця функція завантажує файл асинхронно, тому ваша програма може здійснювати інші операції, поки файл закачується.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`remote_filename`

Шлях до віддаленого файлу.

`stream`

Відкритий файловий дескриптор локального файлу. Читання припиняється при досягненні кінця файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, либо\*\*`FTP_BINARY`\*\*

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`**или**`FTP_MOREDATA`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Пример #1 Пример использования**ftp\_nb\_fput()\*\*\*\*

```php
<?php

$file = 'index.php';

$fp = fopen($file, 'r');

$ftp = ftp_connect($ftp_server);

$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// Начало загрузки
$ret = ftp_nb_fput($ftp, $file, $fp, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // производим какие-то действия ...
   echo ".";

   // продолжение загрузки ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При загрузке файла произошла ошибка...";
   exit(1);
}

fclose($fp);
?>
```

### Дивіться також

-   [ftp\_nb\_put()](function.ftp-nb-put.md) \- Завантажує файл на сервер FTP в асинхронному режимі
-   [ftp\_nb\_continue()](function.ftp-nb-continue.md) \- Продовжує асинхронну операцію
-   [ftp\_put()](function.ftp-put.md) \- Завантажує файл на FTP-сервер
-   [ftp\_fput()](function.ftp-fput.md) \- Завантажує попередньо відкритий файл на FTP-сервер
