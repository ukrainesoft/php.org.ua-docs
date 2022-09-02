---
navigation:
  - function.mysql-get-client-info.md: « mysqlgetclientinfo
  - function.mysql-get-proto-info.md: mysqlgetprotoinfo »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlgethostinfo
---
# mysqlgethostinfo

(PHP 4> = 4.0.5, PHP 5)

mysqlgethostinfo — Повертає інформацію про з'єднання з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqligethostinfo()](mysqli.get-host-info.md)
-   [PDO::getAttribute(PDO::ATTRCONNECTIONSTATUS)](pdo.getattribute.md)

### Опис

```methodsynopsis
mysql_get_host_info(resource $link_identifier = NULL): string|false
```

Описує тип використовуваної сполуки, вказаної переданим дескриптором з'єднання, включаючи ім'я хоста.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає рядок, що описує тип використовуваної сполуки, вказаної переданим дескриптором з'єднання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlgethostinfo()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Тип соединения с MySQL: %s\n", mysql_get_host_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Тип соединения с MySQL: Localhost via UNIX socket
```

### Дивіться також

-   [mysqlgetclientinfo()](function.mysql-get-client-info.md) - Повертає дані про MySQL-клієнт
-   [mysqlgetprotoinfo()](function.mysql-get-proto-info.md) - Повертає інформацію про протокол MySQL
-   [mysqlgetserverinfo()](function.mysql-get-server-info.md) - Повертає інформацію про сервер MySQL
