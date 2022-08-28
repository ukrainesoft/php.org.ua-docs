Повертає докладний список файлів у заданій директорії

-   [« ftp\_raw](function.ftp-raw.html)
    
-   [ftp\_rename »](function.ftp-rename.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Повертає докладний список файлів у заданій директорії
    

# ftprawlist

(PHP 4, PHP 5, PHP 7, PHP 8)

ftprawlist — Повертає докладний список файлів у заданій директорії

### Опис

```methodsynopsis
ftp_rawlist(FTP\Connection $ftp, string $directory, bool $recursive = false): array|false
```

**ftprawlist()** відправляє FTP-серверу команду **LIST** та повертає результат у вигляді масиву.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`directory`

Ім'я директорії на сервері. Може включати аргументи для команди **LIST**

`recursive`

Якщо передано значення **`true`**, серверу буде відправлено команду **LIST-R**

### Значення, що повертаються

Повертає масив, кожен елемент якого містить один рядок відповіді сервера. Повертає **`false`**, якщо передана директорія `directory` не валідна.

Відповідь сервера не обробляється. Для визначення того, як слід інтерпретувати результат, можна використовувати результат роботи функції [ftp\_systype()](function.ftp-systype.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftprawlist()****

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// получение списка файлов директории /
$buff = ftp_rawlist($ftp, '/');

// закрытие соединения
ftp_close($ftp);

// вывод буфера
var_dump($buff);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [ftp\_nlist()](function.ftp-nlist.html) - Повертає список файлів у заданій директорії
-   [ftp\_mlsd()](function.ftp-mlsd.html) - Повертає список файлів у заданій директорії