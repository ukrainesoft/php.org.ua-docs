---
navigation:
  - function.ftp-pasv.md: « ftp\_pasv
  - function.ftp-pwd.md: ftp\_pwd »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_put
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_put

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_put — Завантажує файл на сервер FTP

### Опис

```methodsynopsis
ftp_put(    FTP\Connection $ftp,    string $remote_filename,    string $local_filename,    int $mode = FTP_BINARY,    int $offset = 0): bool
```

**ftp\_put()** завантажує локальний файл на сервер FTP.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`remote_filename`

Шлях до файлу на сервері FTP.

`local_filename`

Шлях до локального файлу.

`mode`

Визначає режим передачі. Може приймати значення **`FTP_ASCII`** або **`FTP_BINARY`**

`offset`

Задає позицію у віддаленому файлі, в яку розпочнеться завантаження

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 7.3.0 | Тепер параметр `mode` опціональний. Раніше він був обов'язковим. |

### Приклади

**Приклад #1 Приклад використання** ftp\_put()\*\*\*\*

```php
<?php
$file = 'somefile.txt';
$remote_file = 'readme.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// загрузка файла
if (ftp_put($ftp, $remote_file, $file, FTP_ASCII)) {
 echo "$file успешно загружен на сервер\n";
} else {
 echo "Не удалось загрузить $file на сервер\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_pasv()](function.ftp-pasv.md) \- Вмикає або вимикає пасивний режим
-   [ftp\_fput()](function.ftp-fput.md) \- Завантажує попередньо відкритий файл на FTP-сервер
-   [ftp\_nb\_fput()](function.ftp-nb-fput.md) \- Завантажує заздалегідь відкритий файл на FTP-сервер в асинхронному режимі
-   [ftp\_nb\_put()](function.ftp-nb-put.md) \- Завантажує файл на сервер FTP в асинхронному режимі
