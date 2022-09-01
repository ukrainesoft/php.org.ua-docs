---
navigation:
  - function.pg-field-type-oid.html: « pgfieldtypeoid
  - function.pg-flush.html: пгflush »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfieldtype
---
# пгfieldtype

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгfieldtype — Повертає ім'я типу заданого поля

### Опис

```methodsynopsis
pg_field_type(PgSql\Result $result, int $field): string
```

**пгfieldtype()** повертає рядок, який містить ім'я базового типу значень колонки результату запиту `result` з номером `field`

> **Зауваження**
> 
> Якщо в якості типу значень використовується PostgreSQL домен (замість базового типу), функція поверне ім'я типу всередині домену, а не ім'я домену.

> **Зауваження**
> 
> Колишня назва функції: **пгfieldtype()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.md) (між іншим).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

Рядок, що містить ім'я базового типу значень поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поле вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

  // Положим, 'title' имеет тип varchar
  $res = pg_query($dbconn, "select title from authors where author = 'Orwell'");

  echo "Title field type: ", pg_field_type($res, 0);
?>
```

Результат виконання цього прикладу:

```
Title field type: varchar
```

### Дивіться також

-   [пгfieldprtlen()](function.pg-field-prtlen.md) - Повертає кількість друкованих символів
-   [пгfieldname()](function.pg-field-name.md) - Повертає найменування поля
-   [пгfieldtypeoid()](function.pg-field-type-oid.md) - Повертає ідентифікатор типу заданого поля
