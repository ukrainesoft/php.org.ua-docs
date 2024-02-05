---
navigation:
  - function.ftp-raw.md: « ftp\_raw
  - function.ftp-rename.md: ftp\_rename »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_rawlist
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_rawlist

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_rawlist — Повертає докладний список файлів у заданій директорії

### Опис

```methodsynopsis
ftp_rawlist(FTP\Connection $ftp, string $directory, bool $recursive = false): array|false
```

**ftp\_rawlist()**отправляет FTP-серверу команду**LIST** та повертає результат у вигляді масиву.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`directory`

Ім'я директорії на сервері. Може включати аргументи для команди **LIST**

`recursive`

Якщо передано значення **`true`**, серверу будет отправлена команда**LIST -R**

### Значення, що повертаються

Повертає масив, кожен елемент якого містить один рядок відповіді сервера. Повертає **`false`**, якщо передана директорія `directory` не валідна.

Відповідь сервера не обробляється. Для визначення того, як слід інтерпретувати результат, можна використовувати результат роботи функції [ftp\_systype()](function.ftp-systype.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_rawlist()\*\*\*\*

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получение списка файлов директории /
$buff = ftp_rawlist($ftp, '/');

// закрытие соединения
ftp_close($ftp);

// вывод буфера
var_dump($buff);
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  string(65) "drwxr-x---   3 vincent  vincent      4096 Jul 12 12:16 public_ftp"
  [1]=>
  string(66) "drwxr-x---  15 vincent  vincent      4096 Nov  3 21:31 public_html"
  [2]=>
  string(73) "lrwxrwxrwx   1 vincent  vincent        11 Jul 12 12:16 www -> public_html"
}
```

### Дивіться також

-   [ftp\_nlist()](function.ftp-nlist.md) \- Повертає список файлів у заданій директорії
-   [ftp\_mlsd()](function.ftp-mlsd.md) \- Повертає список файлів у заданій директорії
