---
navigation:
  - mysqli.get-client-info.html: '« mysqli::$clientinfo'
  - mysqli.get-connection-stats.html: 'mysqli::getconnectionstats »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::$clientversion'
---
# mysqli::$clientversion

# mysqligetclientversion

(PHP 5, PHP 7, PHP 8)

mysqli::$clientversion -- mysqligetclientversion — Повертає інформацію про клієнта MySQL у вигляді рядка

### Опис

Об'єктно-орієнтований стиль

int [$mysqli->clientversion](mysqli.get-client-version.html)

Процедурний стиль

```methodsynopsis
mysqli_get_client_version(): int
```

Повертає версію клієнта як цілого числа.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число, що містить версію клієнтської бібліотеки MySQL у такому форматі: `main_version*10000 + minor_version *100 + sub_version`. Наприклад, для версії 4.1.0 виведе 40100.

Доцільно використовуватиме швидкого визначення версії клієнтської бібліотеки та можливостей її застосування.

### Приклади

**Приклад #1 mysqligetclientversion**

```php
<?php

/* Для определения версии клиентской библиотеки MySQL
 нет необходимости в создании соединения*/

printf("Версия клиентской библиотеки: %d\n", mysqli_get_client_version());
?>
```

### Дивіться також

-   [mysqligetclientinfo()](mysqli.get-client-info.html) - Отримує інформацію про клієнта MySQL
-   [mysqligetserverinfo()](mysqli.get-server-info.html) - Повертає версію MySQL сервера
-   [mysqligetserverversion()](mysqli.get-server-version.html) - Повертає версію сервера MySQL, представлену у вигляді integer
