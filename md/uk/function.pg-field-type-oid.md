---
navigation:
  - function.pg-field-table.md: « pg\_field\_table
  - function.pg-field-type.md: pg\_field\_type »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_type\_oid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_type\_oid

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_field\_type\_oid — Повертає ідентифікатор типу заданого поля

### Опис

```methodsynopsis
pg_field_type_oid(PgSql\Result $result, int $field): string|int
```

**pg\_field\_type\_oid()** повертає цілий ідентифікатор базового типу (OID) значень колонки результату запиту `result` з номером `field`

Більш детальну інформацію про тип значень можна отримати, надіславши запит із отриманим OID до системної таблиці PostgreSQL `pg_type`Функция PostgreSQL**format\_type()** перетворює OID на стандартне ім'я типу SQL.

> **Зауваження** :
> 
> Якщо в якості типу значень використовується PostgreSQL домен (замість базового типу), функція поверне OID типу всередині домену, а не OID домену.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

Повертає базовий тип OID значень поля.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с базой");

  // Допустим, 'title' имеет тип varchar
  $res = pg_query($dbconn, "select title from authors where author = 'Orwell'");

  echo "Title field type OID: ", pg_field_type_oid($res, 0);
?>
```

Результат виконання наведеного прикладу:

```
Title field type OID: 1043
```

### Дивіться також

-   [pg\_field\_type()](function.pg-field-type.md) \- Повертає ім'я типу заданого поля
-   [pg\_field\_prtlen()](function.pg-field-prtlen.md) \- Повертає кількість друкованих символів
-   [pg\_field\_name()](function.pg-field-name.md) \- Повертає найменування поля
