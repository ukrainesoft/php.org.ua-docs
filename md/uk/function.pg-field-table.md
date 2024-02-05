---
navigation:
  - function.pg-field-size.md: « pg\_field\_size
  - function.pg-field-type-oid.md: pg\_field\_type\_oid »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_table
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_table

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

pg\_field\_table — Повертає назву або ідентифікатор таблиці, що містить задане поле

### Опис

```methodsynopsis
pg_field_table(PgSql\Result $result, int $field, bool $oid_only = false): string|int|false
```

**pg\_field\_table()** повертає ім'я таблиці, до якої належить задане поле. Якщо як аргумент `oid_only` передається **`true`**, функція поверне oid-ідентифікатор таблиці

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Порядковий номер поля результату запиту з нуля.

`oid_only`

За замовчуванням функція повертає назву таблиці, що містить поле. Якщо параметр `oid_only`равен\*\*`true`\*\*то функція поверне oid таблиці.

### Значення, що повертаються

При успішному завершенні назва таблиці або її oid або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поле вибірки**

```php
<?php
$dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

$res = pg_query($dbconn, "SELECT bar FROM foo");

echo pg_field_table($res, 0);
echo pg_field_table($res, 0, true);

$res = pg_query($dbconn, "SELECT version()");
var_dump(pg_field_table($res, 0));
?>
```

Висновок наведеного прикладу буде схожим на:

```
foo
14379580

bool(false)
```

### Примітки

> **Зауваження** :
> 
> Повернення oid таблиці значно швидше, ніж назви, оскільки визначення назви вимагає виконання додаткового запиту до системної таблиці бази даних.

### Дивіться також

-   [pg\_field\_name()](function.pg-field-name.md) \- Повертає найменування поля
-   [pg\_field\_type()](function.pg-field-type.md) \- Повертає ім'я типу заданого поля
