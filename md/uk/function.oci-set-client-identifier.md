---
navigation:
  - function.oci-set-call-timout.md: « oci\_set\_call\_timeout
  - function.oci-set-client-info.md: oci\_set\_client\_info »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_set\_client\_identifier
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_set\_client\_identifier

(PHP 5 >= 5.3.2, PHP 7, PHP 8, PECL OCI8 >= 1.4.0)

oci\_set\_client\_identifier — Вказує ідентифікатор клієнта

### Опис

```methodsynopsis
oci_set_client_identifier(resource $connection, string $client_id): bool
```

Встановлює ідентифікатор клієнта, який використовується різними компонентами бази даних для ідентифікації різних користувачів тонких клієнтів, які авторизуються у базі даних як один користувач.

Ідентифікатор клієнта реєструється в базі даних під час чергового запиту від PHP, наприклад коли запускається SQL вираз.

Ідентифікатор може бути вилучений, наприклад, за допомогою `SELECT SYS_CONTEXT('USERENV','CLIENT_IDENTIFIER') FROM DUAL`. Адміністративне подання бази даних, таке як `V$SESSION`також містить це значення. Його можна використовувати спільно з `DBMS_MONITOR.CLIENT_ID_TRACE_ENABLE` для трасування та аудиту.

Значення може зберігатися між запитами сторінок, які використовують те саме постійне з'єднання.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [oci\_connect()](function.oci-connect.md) [oci\_pconnect()](function.oci-pconnect.md), или[oci\_new\_connect()](function.oci-new-connect.md)

`client_id`

Заданий користувачем рядок до 64 байт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановлення ідентифікатора клієнта для користувача**

```php
<?php

// Найдём логин пользователя
session_start();
$un = my_validate_session($_SESSION['username']);
$c = oci_connect('myschema', 'welcome', 'localhost/XE');

// Сообщим его базе данных
oci_set_client_identifier($c, $un);

// Следующий запрос к БД заодно установит идентификатор
$s = oci_parse($c, 'select mydata from mytable');
oci_execute($s);

// ...

?>
```

### Примітки

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [oci\_set\_module\_name()](function.oci-set-module-name.md) \- Задає ім'я модулю
-   [oci\_set\_action()](function.oci-set-action.md) \- Вказує ім'я для дії
-   [oci\_set\_client\_info()](function.oci-set-client-info.md) \- Задає інформацію про клієнта
-   [oci\_set\_db\_operation()](function.oci-set-db-operation.md) \- Задає операцію бази даних
