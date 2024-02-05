---
navigation:
  - mysqli.get-client-info.md: '« mysqli::$client\_info'
  - mysqli.get-connection-stats.md: 'mysqli::get\_connection\_stats »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$client\_version'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$client\_version

# mysqli\_get\_client\_version

(PHP 5, PHP 7, PHP 8)

mysqli::$client\_version -- mysqli\_get\_client\_version — Повертає інформацію про клієнта MySQL у вигляді рядка

### Опис

Об'єктно-орієнтований стиль

int[$mysqli->client\_version](mysqli.get-client-version.md)

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

**Приклад #1 mysqli\_get\_client\_version**

```php
<?php

/* Для определения версии клиентской библиотеки MySQL
 нет необходимости в создании соединения*/

printf("Версия клиентской библиотеки: %d\n", mysqli_get_client_version());
?>
```

### Дивіться також

-   [mysqli\_get\_client\_info()](mysqli.get-client-info.md) \- Отримує інформацію про клієнта MySQL
-   [mysqli\_get\_server\_info()](mysqli.get-server-info.md) \- Повертає версію MySQL сервера
-   [mysqli\_get\_server\_version()](mysqli.get-server-version.md) \- Повертає версію сервера MySQL, представлену у вигляді integer
