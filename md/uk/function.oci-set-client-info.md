---
navigation:
  - function.oci-set-client-identifier.html: « ocisetclientidentifier
  - function.oci-set-db-operation.html: ocisetдбoperation »
  - index.html: PHP Manual
  - ref.oci8.html: OCI8 Функции
title: ocisetclientinfo
---
# ocisetclientinfo

(PHP 5> = 5.3.2, PHP 7, PHP 8, PECL OCI8> = 1.4.0)

ocisetclientinfo — Задає інформацію про клієнта

### Опис

```methodsynopsis
oci_set_client_info(resource $connection, string $client_info): bool
```

Зачепить інформацію про клієнта для трасування Oracle.

Інформація про клієнта реєструється в базі даних під час чергового запиту PHP, наприклад, коли запускається SQL вираз.

Клієнтська інформація може бути вилучена з адміністративних уявлень бази даних, таких як `V$SESSION`

Значення можна встановлювати через постійні з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [ociconnect()](function.oci-connect.html) [ocipconnect()](function.oci-pconnect.html), або [ocinewconnect()](function.oci-new-connect.md)

`client_info`

Заданий користувачем рядок до 64 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення клієнтської інформації**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Запись информации о клиенте
oci_set_client_info($c, 'My Application Version 2');

// Код, осуществляющий запрос к БД, например выборка:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);

?>
```

```
// Пока скрипт выполняется, администратор может увидеть клиентскую
// информацию:

sqlplus system/welcome
SQL> select client_info from v$session;
```

### Примітки

> **Зауваження** **Вимога до версії Oracle**
> 
> Ця функція доступна, якщо PHP злінковано з бібліотеками Oracle Database починаючи з версії 10*г* і вище.

**Підказка**

# Продуктивність

У старих версіях OCI8 або бази даних Oracle можна було встановити інформацію про клієнта за допомогою пакета `DBMS_APPLICATION_INFO`. Для цієї мети ефективніше використання функції **ocisetclientinfo()**

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [ocisetmodulename()](function.oci-set-module-name.md) - Задає ім'я модулю
-   [ocisetaction()](function.oci-set-action.md) - Вказує ім'я для дії
-   [ocisetclientidentifier()](function.oci-set-client-identifier.md) - задає ідентифікатор клієнта
-   [ocisetдбoperation()](function.oci-set-db-operation.md) - Задає операцію бази даних
