Створює директорію

-   [« ftpmdtm](function.ftp-mdtm.html)
    
-   [ftpmlsd »](function.ftp-mlsd.html)
    
-   [PHP Manual](index.html)
    
-   [Функції FTP](ref.ftp.html)
    
-   Створює директорію
    

# ftpmkdir

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpmkdir - Створює директорію

### Опис

```methodsynopsis
ftp_mkdir(FTP\Connection $ftp, string $directory): string|false
```

Створює директорію `directory` на FTP-сервері.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`directory`

Ім'я директорії, що створюється.

### Значення, що повертаються

Повертає ім'я щойно створеної директорії у разі успішного виконання або **`false`** в іншому випадку.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо каталог вже існує або відповідні права доступу перешкоджають створенню каталогу.

### список змін

| Версия | Описание                                                                                                                                            |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpmkdir()****

```php
<?php

$dir = 'www';

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// попытка создания директории $dir
if (ftp_mkdir($ftp, $dir)) {
 echo "Создана директория $dir\n";
} else {
 echo "Не удалось создать директорию $dir\n";
}

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftprmdir()](function.ftp-rmdir.html) - видаляє директорію