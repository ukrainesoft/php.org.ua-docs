---
navigation:
  - mysqli.get-charset.md: '« mysqli::getcharset'
  - mysqli.get-client-version.md: 'mysqli::$clientversion »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$clientinfo'
---
# mysqli::$clientinfo

# mysqli::getclientinfo

# mysqligetclientinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$clientinfo -- mysqli::getclientinfo -- mysqligetclientinfo — Отримує інформацію про клієнта MySQL

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->clientinfo](mysqli.get-client-info.md)

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

| Версия | Описание |
| --- | --- |
|  | Виклик функції **mysqligetclientinfo()** з аргументом `mysql` застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|  | Об'єктно-орієнтований стиль виклику методу **mysqli::getclientinfo()** застарів. |

### Приклади

**Приклад #1 mysqligetclientinfo**

```php
<?php

/* Для определения версии клиентской библиотеки MySQL
   нет необходимости в создании соединения */

printf("Версия клиентской библиотеки: %s\n", mysqli_get_client_info());
?>
```

### Дивіться також

-   [mysqligetclientversion()](mysqli.get-client-version.md) - Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqligetserverinfo()](mysqli.get-server-info.md) - Повертає версію MySQL сервера
-   [mysqligetserverversion()](mysqli.get-server-version.md) - Повертає версію сервера MySQL, представлену у вигляді integer
