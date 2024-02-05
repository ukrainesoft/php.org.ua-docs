---
navigation:
  - function.ftp-connect.md: « ftp\_connect
  - function.ftp-exec.md: ftp\_exec »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_delete

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_delete — Видалення файлу на FTP-сервері

### Опис

```methodsynopsis
ftp_delete(FTP\Connection $ftp, string $filename): bool
```

**ftp\_delete()** видаляє файл, заданий аргументом `filename`з FTP-сервера.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`filename`

Видалений файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_delete()\*\*\*\*

```php
<?php
$file = 'public_html/old.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка удалить файл
if (ftp_delete($ftp, $file)) {
 echo "Файл $file удалён\n";
} else {
 echo "Не удалось удалить $file\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```
