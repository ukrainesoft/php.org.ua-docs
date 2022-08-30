Відправляє довільну команду FTP-серверу

-   [« ftpquit](function.ftp-quit.html)
    
-   [ftprawlist »](function.ftp-rawlist.html)
    
-   [PHP Manual](index.md)
    
-   [Функції FTP](ref.ftp.md)
    
-   Відправляє довільну команду FTP-серверу
    

# ftpraw

(PHP 5, PHP 7, PHP 8)

ftpraw — Надсилає довільну команду FTP-серверу

### Опис

```methodsynopsis
ftp_raw(FTP\Connection $ftp, string $command): ?array
```

Відправляє довільну команду `command` FTP-сервер.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`command`

Команда.

### Значення, що повертаються

Повертає відповідь сервера у вигляді масиву рядків або **`null`** у разі виникнення помилки. Функція **ftpraw()** не інтерпретує відповідь сервера і не визначає, чи успішно виконано команду.

### список змін

| Версия | Описание                                                                                                                                          |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Використання **ftpraw()** для входу на FTP-сервер**

```php
<?php
$ftp = ftp_connect("ftp.example.com");

/* То же самое, что:
   ftp_login($ftp, "joeblow", "secret"); */
ftp_raw($ftp, "USER joeblow");
ftp_raw($ftp, "PASS secret");
?>
```

### Дивіться також

-   [ftpexec()](function.ftp-exec.html) - Запитує виконання команди на FTP-сервері