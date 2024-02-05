---
navigation:
  - function.ftp-close.md: « ftp\_close
  - function.ftp-delete.md: ftp\_delete »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_connect

(PHP 4, PHP 5, PHP 7, PHP 8)

ftp\_connect — Встановлює з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_connect(string $hostname, int $port = 21, int $timeout = 90): FTP\Connection|false
```

**ftp\_connect()** встановлює FTP-з'єднання із вказаним сервером `hostname`

### Список параметрів

`hostname`

Адреса FTP-сервера. Цей аргумент не повинен містити слішів наприкінці та префіксу `ftp://`в начале.

`port`

Цей аргумент вказує на альтернативний порт для підключення. Якщо він опущений або встановлений у нуль, то буде використано FTP порт за замовчуванням – 21.

`timeout`

Цей аргумент вказує час очікування в секундах всіх наступних мережевих операцій. Якщо опущено, використовується значення за промовчанням - 90 секунд. Час очікування може бути змінено та отримано у будь-який момент за допомогою функцій [ftp\_set\_option()](function.ftp-set-option.md) і [ftp\_get\_option()](function.ftp-get-option.md)соответственно.

### Значення, що повертаються

Повертає [FTP\\Connection](class.ftp-connection.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше повертався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_connect()\*\*\*\*

```php
<?php

$ftp_server = "ftp.example.com";

// устанавливает соединение или выходит
$ftp = ftp_connect($ftp_server) or die("Не удалось установить соединение с $ftp_server");

?>
```

### Дивіться також

-   [ftp\_close()](function.ftp-close.md) \- Закриває з'єднання з FTP-сервером
-   [ftp\_ssl\_connect()](function.ftp-ssl-connect.md) \- Встановлює з'єднання з FTP-сервером через SSL
