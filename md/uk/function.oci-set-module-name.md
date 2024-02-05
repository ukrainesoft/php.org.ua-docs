---
navigation:
  - function.oci-set-edition.md: « oci\_set\_edition
  - function.oci-set-prefetch-lob.md: oci\_set\_prefetch\_lob »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_set\_module\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_set\_module\_name

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL OCI8 >= 1.4.0)

oci\_set\_module\_name — Вказує ім'я модуля

### Опис

```methodsynopsis
oci_set_module_name(resource $connection, string $name): bool
```

Вказує ім'я модуля для трасування Oracle.

Ім'я модуля реєструється в базі даних під час чергового запиту від PHP, наприклад коли запускається SQL вираз.

Ім'я може бути витягнуте з адміністративних уявлень бази даних, таких як `V$SESSION`. Воно може використовуватися для трасування та моніторингу також, як `V$SQLAREA`and`DBMS_MONITOR.SERV_MOD_ACT_STAT_ENABLE`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [oci\_connect()](function.oci-connect.md) [oci\_pconnect()](function.oci-pconnect.md), или[oci\_new\_connect()](function.oci-new-connect.md)

`name`

Заданий користувачем рядок string довжиною до 48 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановлення імені модуля**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись модуля
oci_set_module_name($c, 'Home Page');

// Код, осуществляющий запрос к БД, наПриклад выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);
?>
```

```
// Пока скрипт выполняется, администратор может увидеть, какие модули
// используются:

sqlplus system/welcome
SQL> select module from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*g* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції [oci\_set\_client\_info()](function.oci-set-client-info.md)

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [oci\_set\_action()](function.oci-set-action.md) \- Вказує ім'я для дії
-   [oci\_set\_client\_info()](function.oci-set-client-info.md) \- Задає інформацію про клієнта
-   [oci\_set\_client\_identifier()](function.oci-set-client-identifier.md) \- задає ідентифікатор клієнта
-   [oci\_set\_db\_operation()](function.oci-set-db-operation.md) \- Задає операцію бази даних
