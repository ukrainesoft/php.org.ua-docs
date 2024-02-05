---
navigation:
  - function.ftp-fget.md: « ftp\_fget
  - function.ftp-get-option.md: ftp\_get\_option »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_fput
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_fput

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_fput — Завантажує попередньо відкритий файл на сервер FTP

### Опис

```methodsynopsis
ftp_fput(    FTP\Connection $ftp,    string $remote_filename,    resource $stream,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftp\_fput()** завантажує дані із файлового дескриптора у віддалений файл на FTP-сервері.

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання** ftp\_fput()\*\*\*\*

```php
<?php

// открыть файл для чтения
$file = 'somefile.txt';
$fp = fopen($file, 'r');

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка загрузки файла
if (ftp_fput($ftp, $file, $fp, FTP_ASCII)) {
    echo "Файл $file успешно загружен\n";
} else {
    echo "При загрузке $file произошла проблема\n";
}

// закрываем соединение и дескриптор файла
ftp_close($ftp);
fclose($fp);

?>
```

### Дивіться також

-   [ftp\_put()](function.ftp-put.md) \- Завантажує файл на FTP-сервер
-   [ftp\_nb\_fput()](function.ftp-nb-fput.md) \- Завантажує заздалегідь відкритий файл на FTP-сервер в асинхронному режимі
-   [ftp\_nb\_put()](function.ftp-nb-put.md) \- Завантажує файл на сервер FTP в асинхронному режимі
