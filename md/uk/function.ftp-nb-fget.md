---
navigation:
  - function.ftp-nb-continue.md: « ftp\_nb\_continue
  - function.ftp-nb-fput.md: ftp\_nb\_fput »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_nb\_fget
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_nb\_fget

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

ftp\_nb\_fget — Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі

### Опис

```methodsynopsis
ftp_nb_fget(    FTP\Connection $ftp,    resource $stream,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): int
```

**ftp\_nb\_fget()** завантажує віддалений файл із FTP-сервера.

Різниця між цією функцією та [ftp\_fget()](function.ftp-fget.md) полягає в тому, що ця функція отримує файл асинхронно, так що ваша програма може здійснювати інші операції, поки файл завантажується.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`stream`

Відкритий файловий дескриптор для збереження даних.

`remote_filename`

Шлях до віддаленого файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, либо\*\*`FTP_BINARY`\*\*

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`FTP_FAILED`** **`FTP_FINISHED`** або **`FTP_MOREDATA`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання** ftp\_nb\_fget()\*\*\*\*

```php
<?php

// открыть файл для записи
$file = 'index.php';
$fp = fopen($file, 'w');

$ftp = ftp_connect($ftp_server);

$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// Начало скачивания
$ret = ftp_nb_fget($ftp, $fp, $file, FTP_BINARY);
while ($ret == FTP_MOREDATA) {

   // производим какие-то действия ...
   echo ".";

   // продолжение скачивания ...
   $ret = ftp_nb_continue($ftp);
}
if ($ret != FTP_FINISHED) {
   echo "При скачивании файла произошла ошибка...";
   exit(1);
}

// закрытие файла
fclose($fp);
?>
```

### Дивіться також

-   [ftp\_nb\_get()](function.ftp-nb-get.md) \- Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
-   [ftp\_nb\_continue()](function.ftp-nb-continue.md) \- Продовжує асинхронну операцію
-   [ftp\_fget()](function.ftp-fget.md) \- Завантажує файл з FTP-сервера та зберігає його у попередньо відкритому файлі
-   [ftp\_get()](function.ftp-get.md) \- Завантажує файл із FTP-сервера
