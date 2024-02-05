---
navigation:
  - mysqli.get-charset.md: '« mysqli::get\_charset'
  - mysqli.get-client-version.md: 'mysqli::$client\_version »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$client\_info'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$client\_info

# mysqli::get\_client\_info

# mysqli\_get\_client\_info

(PHP 5, PHP 7, PHP 8)

mysqli::$client\_info -- mysqli::get\_client\_info -- mysqli\_get\_client\_info — Отримує інформацію про клієнта MySQL

### Опис

Об'єктно-орієнтований стиль

string[$mysqli->client\_info](mysqli.get-client-info.md)

```methodsynopsis
public mysqli::get_client_info(): string
```

Процедурний стиль

```methodsynopsis
mysqli_get_client_info(?mysqli $mysql = null): string
```

Повертає рядок, що містить версію клієнтської бібліотеки MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок, що містить версію клієнтської бібліотеки MySQL.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Виклик функції **mysqli\_get\_client\_info()** з аргументом `mysql` застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
| 8.1.0 | Об'єктно-орієнтований стиль виклику методу \*\*mysqli::get\_client\_info()\*\*устарел. |

### Приклади

**Приклад #1 mysqli\_get\_client\_info**

```php
<?php

/* Для определения версии клиентской библиотеки MySQL
   нет необходимости в создании соединения */

printf("Версия клиентской библиотеки: %s\n", mysqli_get_client_info());
?>
```

### Дивіться також

-   [mysqli\_get\_client\_version()](mysqli.get-client-version.md) \- Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqli\_get\_server\_info()](mysqli.get-server-info.md) \- Повертає версію MySQL сервера
-   [mysqli\_get\_server\_version()](mysqli.get-server-version.md) \- Повертає версію сервера MySQL, представлену у вигляді integer
