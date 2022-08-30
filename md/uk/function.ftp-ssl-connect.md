Встановлює з'єднання з FTP-сервером через SSL

-   [« ftpsize](function.ftp-size.html)
    
-   [ftpsystype »](function.ftp-systype.html)
    
-   [PHP Manual](index.html)
    
-   [Функції FTP](ref.ftp.html)
    
-   Встановлює з'єднання з FTP-сервером через SSL
    

# ftpsslconnect

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

ftpsslconnect — Встановлює з'єднання з FTP-сервером через SSL

### Опис

```methodsynopsis
ftp_ssl_connect(string $hostname, int $port = 21, int $timeout = 90): FTP\Connection|false
```

**ftpsslconnect()** встановлює *явне* SSL з'єднання з FTP-сервером, заданим аргументом `hostname`. Це означає, що **ftpsslconnect()** буде успішним навіть якщо сервер не налаштований для SSL-FTP, або його сертифікат недійсний. Тільки коли буде викликана функція [ftplogin()](function.ftp-login.html), клієнт надішле необхідну команду AUTH FTP, так що у зазначених випадках [ftplogin()](function.ftp-login.html) завершиться помилкою.

> **Зауваження** **Чому ця функція може бути не визначена**
> 
> До PHP 7.0.0 **ftpsslconnect()** була доступна тільки якщо PHP був зібраний з підтримкою [OpenSSL](ref.openssl.html); це означає, що у Windows ця функція не була визначена в офіційних збірках PHP. Щоб використовувати цю функцію під Windows, вам доведеться зібрати PHP самостійно, щоб увімкнути підтримку OpenSSL.

> **Зауваження**
> 
> **ftpsslconnect()** не призначена для використання протоколу sFTP. Для використання sFTP із PHP дивіться функцію [ssh2sftp()](function.ssh2-sftp.html)

### Список параметрів

`hostname`

Адреса FTP-сервера. Цей параметр не повинен містити сліші в кінці та префікс `ftp://` на початку.

`port`

Задає порт, у якому встановлюється з'єднання. Якщо дорівнює нулю або опущений, використовується стандартний для протоколу FTP - порт 21.

`timeout`

Задає час очікування для всіх операцій із цим з'єднанням. За замовчуванням час очікування встановлюється за 90 секунд. Отримати та встановити значення часу очікування можна також за допомогою функцій [ftpsetoption()](function.ftp-set-option.html) і [ftpgetoption()](function.ftp-get-option.html)

### Значення, що повертаються

Повертає [FTPConnection](class.ftp-connection.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                          |
|--------|-----------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [FTPConnection](class.ftp-connection.html); раніше повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання функції **ftpsslconnect()****

```php
<?php

// установка ssl-соединения
$ftp = ftp_ssl_connect($ftp_server);

// проверка имени пользователя и пароля
$login_result = ftp_login($ftp, $ftp_user_name, $ftp_user_pass);

if (!$login_result) {
    // В этом случае PHP уже выбросил сообщение уровня E_WARNING
    die("can't login");
}

echo ftp_pwd($ftp); // /

// закрытие ssl-соединения
ftp_close($ftp);
?>
```

### Дивіться також

-   [ftpconnect()](function.ftp-connect.html) - Встановлює з'єднання з FTP-сервером