---
navigation:
  - function.mysql-get-host-info.md: « mysql\_get\_host\_info
  - function.mysql-get-server-info.md: mysql\_get\_server\_info »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_get\_proto\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_get\_proto\_info

(PHP 4 >= 4.0.5, PHP 5)

mysql\_get\_proto\_info — Повертає інформацію про протокол MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_get\_proto\_info()](mysqli.get-proto-info.md)

### Опис

```methodsynopsis
mysql_get_proto_info(resource $link_identifier = NULL): int|false
```

Повертає інформацію про протокол MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає використовуваний протокол MySQL у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_get\_proto\_info()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Версия протокола MySQL: %s\n", mysql_get_proto_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Версия протокола MySQL: 10
```

### Дивіться також

-   [mysql\_get\_client\_info()](function.mysql-get-client-info.md) \- Повертає дані про MySQL-клієнт
-   [mysql\_get\_host\_info()](function.mysql-get-host-info.md) \- Повертає інформацію про з'єднання з MySQL
-   [mysql\_get\_server\_info()](function.mysql-get-server-info.md) \- Повертає інформацію про сервер MySQL
