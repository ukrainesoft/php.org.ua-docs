---
navigation:
  - function.oci-server-version.md: « ociserverversion
  - function.oci-set-call-timout.md: ocisetcalltimeout »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocisetaction
---
# ocisetaction

(PHP 5> = 5.3.2, PHP 7, PHP 8, PECL OCI8> = 1.4.0)

ocisetaction — Вказує ім'я для дії

### Опис

```methodsynopsis
oci_set_action(resource $connection, string $action): bool
```

Надає ім'я дії для трасування Oracle.

Надане ім'я реєструється в базі даних під час чергового запиту від PHP, наприклад, коли запускається SQL вираз.

Ім'я дії може бути витягнуте з адміністративних уявлень бази даних, таких як `V$SESSION`. Його можна використовувати для трасування та моніторингу, наприклад, за допомогою `V$SQLAREA` і `DBMS_MONITOR.SERV_MOD_ACT_STAT_ENABLE`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [ociconnect()](function.oci-connect.md) [ocipconnect()](function.oci-pconnect.md), або [ocinewconnect()](function.oci-new-connect.md)

`action`

Заданий користувачем рядок до 32 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення дії**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись действия
oci_set_action($c, 'Friend Lookup');

// Код, осуществляющий запрос к БД, например выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);

?>
```

```
// Пока скрипт выполняется, администратор может наблюдать выполнение действий:

sqlplus system/welcome
SQL> select action from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*г* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції [ocisetclientinfo()](function.oci-set-client-info.md)

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [ocisetmodulename()](function.oci-set-module-name.md) - Задає ім'я модулю
-   [ocisetclientinfo()](function.oci-set-client-info.md) - Задає інформацію про клієнта
-   [ocisetclientidentifier()](function.oci-set-client-identifier.md) - задає ідентифікатор клієнта
-   [ocisetдбoperation()](function.oci-set-db-operation.md) - Задає операцію бази даних
