---
navigation:
  - function.ftp-nb-put.md: « ftp\_nb\_put
  - function.ftp-pasv.md: ftp\_pasv »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_nlist
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_nlist

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_nlist — Повертає список файлів у заданій директорії

### Опис

```methodsynopsis
ftp_nlist(FTP\Connection $ftp, string $directory): array|false
```

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`directory`

Ім'я каталогу для отримання списку файлів. Цей параметр також може містити аргументи, наприклад `ftp_nlist($conn_id, "-la /your/dir");`. Зверніть увагу, що цей параметр не проходить екранування спецсимволів, тому можуть виникнути проблеми з іменами, що містять пробіли та інші подібні символи.

### Значення, що повертаються

Повертає масив імен файлів у директорії або \*\*`false`\*\*при возникновении ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_nlist()\*\*\*\*

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получить содержимое текущей директории
$contents = ftp_nlist($v, ".");

// вывод $contents
var_dump($contents);

?>
```

Наведений вище приклад виведе:

```
array(3) {
  [0]=>
  string(11) "public_html"
  [1]=>
  string(10) "public_ftp"
  [2]=>
  string(3) "www"
```

### Дивіться також

-   [ftp\_rawlist()](function.ftp-rawlist.md) \- Повертає докладний список файлів у заданій директорії
-   [ftp\_mlsd()](function.ftp-mlsd.md) \- Повертає список файлів у заданій директорії
