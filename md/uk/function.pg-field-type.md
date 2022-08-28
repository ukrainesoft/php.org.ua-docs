Повертає ім'я типу заданого поля

-   [« pg\_field\_type\_oid](function.pg-field-type-oid.html)
    
-   [pg\_flush »](function.pg-flush.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає ім'я типу заданого поля
    

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

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

Рядок, що містить ім'я базового типу значень поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_field\_prtlen()](function.pg-field-prtlen.html) - Повертає кількість друкованих символів
-   [pg\_field\_name()](function.pg-field-name.html) - Повертає найменування поля
-   [pg\_field\_type\_oid()](function.pg-field-type-oid.html) - Повертає ідентифікатор типу заданого поля