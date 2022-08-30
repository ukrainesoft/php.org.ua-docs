Видаляє директорію

-   [« ftprename](function.ftp-rename.html)
    
-   [ftpsetoption »](function.ftp-set-option.html)
    
-   [PHP Manual](index.html)
    
-   [Функції FTP](ref.ftp.html)
    
-   Видаляє директорію
    

# ftprmdir

(PHP 4, PHP 5, PHP 7, PHP 8)

ftprmdir - Видаляє директорію

### Опис

```methodsynopsis
ftp_rmdir(FTP\Connection $ftp, string $directory): bool
```

Видаляє директорію `directory`

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`directory`

Ім'я директорії. Параметр повинен мати відносний або абсолютний шлях до порожньої директорії.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                            |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftprmdir()****

```php
<?php

$dir = 'www/';

// установка соединения
$ftp = ftp_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка удаления директории $dir
if (ftp_rmdir($ftp, $dir)) {
    echo "Директория $dir удалена\n";
} else {
    echo "Не удалось удалить директорию $dir\n";
}

ftp_close($ftp);

?>
```

### Дивіться також

-   [ftpmkdir()](function.ftp-mkdir.html) - створює директорію