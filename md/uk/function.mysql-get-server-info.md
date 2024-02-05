---
navigation:
  - function.mysql-get-proto-info.md: « mysql\_get\_proto\_info
  - function.mysql-info.md: mysql\_info »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_get\_server\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_get\_server\_info

(PHP 4 >= 4.0.5, PHP 5)

mysql\_get\_server\_info — Повертає інформацію про сервер MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_get\_server\_info()](mysqli.get-server-info.md)
-   [PDO::getAttribute()](pdo.getattribute.md)с параметром`attribute`заданим як\*\*`PDO::ATTR_SERVER_VERSION`\*\*

### Опис

```methodsynopsis
mysql_get_server_info(resource $link_identifier = NULL): string|false
```

Повертає версію MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає версію сервера MySQL у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mysql\_get\_server\_info()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Версия сервера MySQL: %s\n", mysql_get_server_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Версия сервера MySQL: 4.0.1-alpha
```

### Дивіться також

-   [mysql\_get\_client\_info()](function.mysql-get-client-info.md) \- Повертає дані про MySQL-клієнт
-   [mysql\_get\_host\_info()](function.mysql-get-host-info.md) \- Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_proto\_info()](function.mysql-get-proto-info.md) \- Повертає інформацію про протокол MySQL
-   [phpversion()](function.phpversion.md) \- Отримує поточну версію PHP
