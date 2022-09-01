---
navigation:
  - function.ftp-connect.html: « ftpconnect
  - function.ftp-exec.html: ftpexec »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpdelete
---
# ftpdelete

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpdelete — Видалення файлу на FTP-сервері

### Опис

```methodsynopsis
ftp_delete(FTP\Connection $ftp, string $filename): bool
```

**ftpdelete()** видаляє файл, заданий аргументом `filename`з FTP-сервера.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`filename`

Видалений файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpdelete()****

```php
<?php
$file = 'public_html/old.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка удалить файл
if (ftp_delete($ftp, $file)) {
 echo "Файл $file удалён\n";
} else {
 echo "Не удалось удалить $file\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```
