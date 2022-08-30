Переходить до батьківської директорії

-   [« ftpappend](function.ftp-append.html)
    
-   [ftpchdir »](function.ftp-chdir.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Переходить до батьківської директорії
    

# ftpcdup

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpcdup - Переходить до батьківської директорії

### Опис

```methodsynopsis
ftp_cdup(FTP\Connection $ftp): bool
```

Переходить у батьківську директорію.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання функції **ftpcdup()****

```php
<?php
// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// изменение текущей директории на html
ftp_chdir($ftp, 'html');

echo ftp_pwd($ftp); // /html

// возврат в родительскую директорию
if (ftp_cdup($ftp)) {
  echo "команда cdup выполнена успешно\n";
} else {
  echo "команда cdup завершилась неудачей\n";
}

echo ftp_pwd($ftp); // /

ftp_close($ftp);
?>
```

### Дивіться також

-   [ftpchdir()](function.ftp-chdir.html) - Змінює поточну директорію на FTP-сервері
-   [ftppwd()](function.ftp-pwd.html) - Повертає ім'я поточної директорії