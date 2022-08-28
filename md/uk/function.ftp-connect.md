Встановлює з'єднання з сервером FTP

-   [« ftp\_close](function.ftp-close.html)
    
-   [ftp\_delete »](function.ftp-delete.html)
    
-   [PHP Manual](index.html)
    
-   [Функции FTP](ref.ftp.html)
    
-   Встановлює з'єднання з сервером FTP
    

# ftpconnect

(PHP 4, PHP 5, PHP 7, PHP 8)

ftpconnect — Встановлює з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_connect(string $hostname, int $port = 21, int $timeout = 90): FTP\Connection|false
```

**ftpconnect()** встановлює FTP-з'єднання із вказаним сервером `hostname`

### Список параметрів

`hostname`

Адреса FTP-сервера. Цей аргумент не повинен містити слішів наприкінці та префіксу `ftp://` на початку.

`port`

Цей аргумент вказує на альтернативний порт для підключення. Якщо він опущений або встановлений у нуль, то буде використано FTP порт за замовчуванням - 21.

`timeout`

Цей аргумент вказує час очікування в секундах всіх наступних мережевих операцій. Якщо опущено, використовується значення за промовчанням - 90 секунд. Час очікування може бути змінено та отримано у будь-який момент за допомогою функцій [ftp\_set\_option()](function.ftp-set-option.html) і [ftp\_get\_option()](function.ftp-get-option.html) відповідно.

### Значення, що повертаються

Повертає [FTP\\Connection](class.ftp-connection.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                            |
|--------|-------------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [FTP\\Connection](class.ftp-connection.html); раніше повертався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpconnect()****

```php
<?php

$ftp_server = "ftp.example.com";

// устанавливает соединение или выходит
$ftp = ftp_connect($ftp_server) or die("Не удалось установить соединение с $ftp_server");

?>
```

### Дивіться також

-   [ftp\_close()](function.ftp-close.html) - Закриває з'єднання з FTP-сервером
-   [ftp\_ssl\_connect()](function.ftp-ssl-connect.html) - Встановлює з'єднання з FTP-сервером через SSL