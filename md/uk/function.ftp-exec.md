Запитує виконання команди на FTP-сервері

-   [« ftp\_delete](function.ftp-delete.html)
    
-   [ftp\_fget »](function.ftp-fget.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Запитує виконання команди на FTP-сервері
    

# ftpexec

(PHP 4> = 4.0.3, PHP 5, PHP 7, PHP 8)

ftpexec — Вимагає виконання команди на FTP-сервері

### Опис

```methodsynopsis
ftp_exec(FTP\Connection $ftp, string $command): bool
```

Надсилає команду SITE EXEC `command` на сервері FTP.

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

`command`

Команда для виконання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання команди (сервер надсилає код відповіді: `200`); в іншому випадку повертає **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpexec()****

```php
<?php
// инициализация переменных
$command = 'ls -al >files.txt';

// устанавливаем соединение
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// выполняем команду
if (ftp_exec($ftp, $command)) {
    echo "Команда $command выполнена успешно\n";
} else {
    echo "Не удалось выполнить $command\n";
}

// закрываем соединение
ftp_close($ftp);

?>
```

### Дивіться також

-   [ftp\_raw()](function.ftp-raw.html) - Надсилає довільну команду FTP-серверу