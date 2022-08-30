Отримує інформацію про клієнта MySQL

-   [« mysqli::getcharset](mysqli.get-charset.html)
    
-   [mysqli::$clientversion »](mysqli.get-client-version.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Отримує інформацію про клієнта MySQL
    

# mysqli::$clientinfo

# mysqli::getclientinfo

# mysqligetclientinfo

(PHP 5, PHP 7, PHP 8)

mysqli::$clientinfo -- mysqli::getclientinfo -- mysqligetclientinfo — Отримує інформацію про клієнта MySQL

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->clientinfo](mysqli.get-client-info.html)

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

| Версия | Описание                                                                                                                                                                 |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Виклик функції **mysqligetclientinfo()** з аргументом `mysql` застарів. Функція ніколи не вимагала параметра, але неправильно дозволяла його як необов'язковий параметр. |
|        | Об'єктно-орієнтований стиль виклику методу **mysqli::getclientinfo()** застарів.                                                                                         |

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

-   [mysqligetclientversion()](mysqli.get-client-version.html) - Повертає інформацію про клієнта MySQL у вигляді рядка
-   [mysqligetserverinfo()](mysqli.get-server-info.html) - Повертає версію MySQL сервера
-   [mysqligetserverversion()](mysqli.get-server-version.html) - Повертає версію сервера MySQL, представлену у вигляді integer