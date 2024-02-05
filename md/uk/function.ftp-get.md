---
navigation:
  - function.ftp-get-option.md: « ftp\_get\_option
  - function.ftp-login.md: ftp\_login »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_get

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_get — Завантажує файл із FTP-сервера

### Опис

```methodsynopsis
ftp_get(    FTP\Connection $ftp,    string $local_filename,    string $remote_filename,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftp\_get()** завантажує видалений файл з сервера FTP і зберігає його локально.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`local_filename`

Шлях до локального файлу (файл буде перезаписано, якщо існує).

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

**Приклад #1 Приклад використання** ftp\_get()\*\*\*\*

```php
<?php

// объявление переменных
$local_file = 'local.zip';
$server_file = 'server.zip';

// установка соединения
$conn_id = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($conn_id, $ftp_user_name, $ftp_user_pass);

// попытка скачать $server_file и сохранить в $local_file
if (ftp_get($conn_id, $local_file, $server_file, FTP_BINARY)) {
    echo "Произведена запись в $local_file\n";
} else {
    echo "Не удалось завершить операцию\n";
}

// закрытие соединения
ftp_close($conn_id);

?>
```

### Дивіться також

-   [ftp\_pasv()](function.ftp-pasv.md) \- Вмикає або вимикає пасивний режим
-   [ftp\_fget()](function.ftp-fget.md) \- Завантажує файл з FTP-сервера та зберігає його у попередньо відкритому файлі
-   [ftp\_nb\_get()](function.ftp-nb-get.md) \- Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у локальний файл
-   [ftp\_nb\_fget()](function.ftp-nb-fget.md) \- Завантажує файл з FTP-сервера в асинхронному режимі та зберігає його у попередньо відкритому файлі
