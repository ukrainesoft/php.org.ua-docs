---
navigation:
  - function.mysql-get-host-info.md: « mysqlgethostinfo
  - function.mysql-get-server-info.md: mysqlgetserverinfo »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlgetprotoinfo
---
# mysqlgetprotoinfo

(PHP 4> = 4.0.5, PHP 5)

mysqlgetprotoinfo — Повертає інформацію про протокол MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqligetprotoinfo()](mysqli.get-proto-info.md)

### Опис

```methodsynopsis
mysql_get_proto_info(resource $link_identifier = NULL): int|false
```

Повертає інформацію про протокол MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає використовуваний протокол MySQL у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlgetprotoinfo()****

```php
<?php
$link = mysql_connect('localhost', 'mysql_user', 'mysql_password');
if (!$link) {
    die('Ошибка соединения: ' . mysql_error());
}
printf("Версия протокола MySQL: %s\n", mysql_get_proto_info());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Версия протокола MySQL: 10
```

### Дивіться також

-   [mysqlgetclientinfo()](function.mysql-get-client-info.md) - Повертає дані про MySQL-клієнт
-   [mysqlgethostinfo()](function.mysql-get-host-info.md) - Повертає інформацію про з'єднання з MySQL
-   [mysqlgetserverinfo()](function.mysql-get-server-info.md) - Повертає інформацію про сервер MySQL
