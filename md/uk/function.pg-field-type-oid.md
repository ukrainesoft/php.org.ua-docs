---
navigation:
  - function.pg-field-table.md: « pgfieldtable
  - function.pg-field-type.md: пгfieldtype »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfieldtypeoid
---
# пгfieldtypeoid

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгfieldtypeoid — Повертає ідентифікатор типу заданого поля

### Опис

```methodsynopsis
pg_field_type_oid(PgSql\Result $result, int $field): string|int
```

**пгfieldtypeoid()** повертає цілий ідентифікатор базового типу (OID) значень колонки результату запиту `result` з номером `field`

Більш детальну інформацію про тип значень можна отримати, надіславши запит із отриманим OID до системної таблиці PostgreSQL `pg_type`. Функція PostgreSQL **formattype()** перетворює OID на стандартне ім'я типу SQL.

> **Зауваження**
> 
> Якщо тип значень використовується PostgreSQL домен (замість базового типу), функція поверне OID типу всередині домену, а не OID самого домену.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

OID базового типу значень поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поля вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Невозможно соединиться с базой");

  // Допустим, 'title' имеет тип varchar
  $res = pg_query($dbconn, "select title from authors where author = 'Orwell'");

  echo "Title field type OID: ", pg_field_type_oid($res, 0);
?>
```

Результат виконання цього прикладу:

```
Title field type OID: 1043
```

### Дивіться також

-   [пгfieldtype()](function.pg-field-type.md) - Повертає ім'я типу заданого поля
-   [пгfieldprtlen()](function.pg-field-prtlen.md) - Повертає кількість друкованих символів
-   [пгfieldname()](function.pg-field-name.md) - Повертає найменування поля
