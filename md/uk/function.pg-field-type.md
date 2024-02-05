---
navigation:
  - function.pg-field-type-oid.md: « pg\_field\_type\_oid
  - function.pg-flush.md: pg\_flush »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_field\_type
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_field\_type

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_field\_type — Повертає ім'я типу заданого поля

### Опис

```methodsynopsis
pg_field_type(PgSql\Result $result, int $field): string
```

**pg\_field\_type()** повертає рядок, який містить ім'я базового типу значень колонки результату запиту `result` з номером `field`

> **Зауваження** :
> 
> Якщо тип значень використовується PostgreSQL домен (замість базового типу), функція поверне ім'я типу всередині домену, а не ім'я самого домену.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_fieldtype()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

Рядок, що містить ім'я базового типу значень поля.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Отримання інформації про поле вибірки**

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

  // Положим, 'title' имеет тип varchar
  $res = pg_query($dbconn, "select title from authors where author = 'Orwell'");

  echo "Title field type: ", pg_field_type($res, 0);
?>
```

Результат виконання наведеного прикладу:

```
Title field type: varchar
```

### Дивіться також

-   [pg\_field\_prtlen()](function.pg-field-prtlen.md) \- Повертає кількість друкованих символів
-   [pg\_field\_name()](function.pg-field-name.md) \- Повертає найменування поля
-   [pg\_field\_type\_oid()](function.pg-field-type-oid.md) \- Повертає ідентифікатор типу заданого поля
