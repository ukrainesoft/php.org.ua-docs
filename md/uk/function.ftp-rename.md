Перейменовує файл або директорію на FTP-сервері

-   [« ftprawlist](function.ftp-rawlist.html)
    
-   [ftprmdir »](function.ftp-rmdir.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Перейменовує файл або директорію на FTP-сервері
    

# ftprename

(PHP 4, PHP 5, PHP 7, PHP 8)

ftprename — Перейменовує файл або директорію на FTP-сервері

### Опис

```methodsynopsis
ftp_rename(FTP\Connection $ftp, string $from, string $to): bool
```

**ftprename()** перейменовує файл або директорію на сервері FTP.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`from`

Старе ім'я файлу/директорії.

`to`

Нове ім'я

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки. У разі виникнення помилки (наприклад, при спробі перейменувати неіснуючий файл) буде викликана помилка рівня `E_WARNING`

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftprename()****

```php
<?php
$old_file = 'somefile.txt.bak';
$new_file = 'somefile.txt';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка переименовать $olf_file в $new_file
if (ftp_rename($ftp, $old_file, $new_file)) {
 echo "Файл $old_file переименован в $new_file\n";
} else {
 echo "Не удалось переименовать $old_file в $new_file\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```