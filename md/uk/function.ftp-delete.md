Видаляє файл на FTP-сервері

-   [« ftp\_connect](function.ftp-connect.html)
    
-   [ftp\_exec »](function.ftp-exec.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Видаляє файл на FTP-сервері
    

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

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`filename`

Видалений файл.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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