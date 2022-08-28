Закриває з'єднання з FTP-сервером

-   [« ftp\_chmod](function.ftp-chmod.html)
    
-   [ftp\_connect »](function.ftp-connect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Закриває з'єднання з FTP-сервером
    

# ftpclose

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftpclose — Закриває з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_close(FTP\Connection $ftp): bool
```

**ftpclose()** закриває вказаний ідентифікатор з'єднання із сервером та звільняє resource.

> **Зауваження**
> 
> Після виклику цієї функції, з'єднання більше не може бути використане, і при необхідності має бути встановлене заново за допомогою функції [ftp\_connect()](function.ftp-connect.html)

### Список параметрів

`ftp`

Ан [FTP\\Connection](class.ftp-connection.html) instance.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpclose()****

```php
<?php

// установка соединения
$ftp = ftp_connect($ftp_server);

// вход с именем пользователя и паролем
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

// вывод текущей директории
echo ftp_pwd($ftp); // /

// закрытие соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftp\_connect()](function.ftp-connect.html) - Встановлює з'єднання з FTP-сервером