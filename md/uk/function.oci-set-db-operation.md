---
navigation:
  - function.oci-set-client-info.md: « ocisetclientinfo
  - function.oci-set-edition.md: ocisetedition »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocisetдбoperation
---
# ocisetдбoperation

(PHP 7> = 7.2.14, PHP 8, PHP 7> = 7.3.1, PHP 8, PECL OCI8> = 2.2.0)

ocisetдбoperation — Задає операцію бази даних

### Опис

```methodsynopsis
oci_set_db_operation(resource $connection, string $action): bool
```

Встановлює DBOP для трасування Oracle.

Ім'я операції бази даних реєструється в базі даних при наступному "циклічному шляху" (round-trip) з PHP до бази даних, як правило, при виконанні виразу SQL.

Операція бази даних може згодом вимагатися з уявлень адміністрування бази даних, таких як `V$SQL_MONITOR`

Функція **ocisetдбoperation()** доступна, якщо oci8 використовує клієнтські бібліотеки Oracle версії 12 (або новіші) та базу даних Oracle 12 (або новіші).

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, що повертається [ociconnect()](function.oci-connect.md) [ocipconnect()](function.oci-pconnect.md), або [ocinewconnect()](function.oci-new-connect.md)

`action`

Користувальницький рядок.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Встановлення DBOP**

```php
<?php

$c = oci_connect('hr', 'welcome', 'localhost/XE');

// Записать операцию
oci_set_db_operation($c, 'main query');

// Код, вызывающий циклический путь, например запрос:
$s = oci_parse($c, 'select * from dual');
oci_execute($s);
oci_fetch_all($s, $res);

sleep(30);

?>
```

```
// Во время выполнения скрипта администратор может видеть выполняемые операции
// с базой данных.

sqlplus system/welcome
SQL> select dbop_name from v$sql_monitor;
```

### Примітки

**Застереження**

# Порада щодо повного сканування таблиці (roundtrip)

Деякі, але не всі функції OCI8 викликають повне сканування таблиці (roundtrip). Повне сканування таблиць немає для тих запитів, у яких включено кешування результатів у базі даних.

### Дивіться також

-   [ocisetaction()](function.oci-set-action.md) - Вказує ім'я для дії
-   [ocisetmodulename()](function.oci-set-module-name.md) - Задає ім'я модулю
-   [ocisetclientinfo()](function.oci-set-client-info.md) - Задає інформацію про клієнта
-   [ocisetclientidentifier()](function.oci-set-client-identifier.md) - задає ідентифікатор клієнта
