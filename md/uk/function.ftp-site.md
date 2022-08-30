Надсилає серверу команду SITE

-   [« ftpsetoption](function.ftp-set-option.html)
    
-   [ftpsize »](function.ftp-size.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Надсилає серверу команду SITE
    

# ftpsite

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpsite — Надсилає серверу команду SITE

### Опис

```methodsynopsis
ftp_site(FTP\Connection $ftp, string $command): bool
```

**ftpsite()** відправляє вказану команду `SITE` FTP-сервер.

Команди `SITE` не стандартизовані та залежать від FTP-сервера. Вони можуть бути корисними для зміни прав доступу до файлів або зміни власника або групи.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`command`

Команда SITE. Зверніть увагу, що цей параметр не проходить екранування спецсимволів, тому можуть виникнути проблеми з іменами, що містять пробіли та інші подібні символи.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Надсилання команди SITE FTP-серверу**

```php
<?php
// Соединение с FTP-сервером
$ftp = ftp_connect('ftp.example.com');
if (!$conn) die('Не удалось подключиться к ftp.example.com');

// Вход под именем "user" с паролем "pass"
if (!ftp_login($ftp, 'user', 'pass')) die('Не удалось войти на ftp.example.com');

// Отправка "SITE CHMOD 0600 /home/user/privatefile" FTP-серверу
if (ftp_site($ftp, 'CHMOD 0600 /home/user/privatefile')) {
   echo "Команда выполнена.\n";
} else {
   die('Команда не выполнена.');
}
?>
```

### Дивіться також

-   [ftpraw()](function.ftp-raw.html) - Надсилає довільну команду FTP-серверу