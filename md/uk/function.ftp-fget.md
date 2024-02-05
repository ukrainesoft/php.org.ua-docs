---
navigation:
  - function.ftp-exec.md: « ftp\_exec
  - function.ftp-fput.md: ftp\_fput »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_fget
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_fget

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_fget — Завантажує файл із FTP-сервера і зберігає його у попередньо відкритому файлі

### Опис

```methodsynopsis
ftp_fget(    FTP\Connection $ftp,    resource $stream,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftp\_fget()** завантажує файл `remote_filename` з FTP-сервера та записує його в переданий файловий дескриптор.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`stream`

Відкритий файловий дескриптор, у якому буде збережено дані.

`remote_filename`

Шлях до віддаленого файлу.

`mode`

Режим передачі. Має бути або **`FTP_ASCII`**, либо\*\*`FTP_BINARY`\*\*

`offset`

Позиція початку завантаження у віддаленому файлі.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Пример #1 Пример использования**ftp\_fget()\*\*\*\*

```php
<?php

// путь к удалённому файлу
$remote_file = 'somefile.txt';
$local_file = 'localfile.txt';

// открываем файл для записи
$handle = fopen($local_file, 'w');

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// пытаемся скачать файл и сохранить его в $handle
if (ftp_fget($ftp, $handle, $remote_file, FTP_ASCII, 0)) {
 echo "Произведена запись в $local_file\n";
} else {
 echo "При скачивании $remote_file в $local_file произошла проблема\n";
}

// закрытие соединения и локального файла
ftp_close($ftp);
fclose($handle);
?>
```

### Дивіться також

-   [ftp\_get()](function.ftp-get.md) \- Завантажує файл із FTP-сервера
-   [ftp\_nb\_get()](function.ftp-nb-get.md) \- Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
-   [ftp\_nb\_fget()](function.ftp-nb-fget.md) \- Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі
