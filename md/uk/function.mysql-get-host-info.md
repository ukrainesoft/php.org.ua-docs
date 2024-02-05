---
navigation:
  - function.mysql-get-client-info.md: « mysql\_get\_client\_info
  - function.mysql-get-proto-info.md: mysql\_get\_proto\_info »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_get\_host\_info
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_get\_host\_info

(PHP 4 >= 4.0.5, PHP 5)

mysql\_get\_host\_info — Повертає інформацію про з'єднання з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_get\_host\_info()](mysqli.get-host-info.md)
-   [PDO::getAttribute()](pdo.getattribute.md)с параметром`attribute`заданим як\*\*`PDO::ATTR_CONNECTION_STATUS`\*\*

### Опис

```methodsynopsis
mysql_get_host_info(resource $link_identifier = NULL): string|false
```

Описує тип використовуваної сполуки, вказаної переданим дескриптором з'єднання, включаючи ім'я хоста.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок, що описує тип використовуваної сполуки, вказаної переданим дескриптором з'єднання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** mysql\_get\_host\_info()\*\*\*\*

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Тип соединения с MySQL: %s\n", mysql_get_host_info());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Тип соединения с MySQL: Localhost via UNIX socket
```

### Дивіться також

-   [mysql\_get\_client\_info()](function.mysql-get-client-info.md) \- Повертає дані про MySQL-клієнт
-   [mysql\_get\_proto\_info()](function.mysql-get-proto-info.md) \- Повертає інформацію про протокол MySQL
-   [mysql\_get\_server\_info()](function.mysql-get-server-info.md) \- Повертає інформацію про сервер MySQL
