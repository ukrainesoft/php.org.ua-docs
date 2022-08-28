Повертає ідентифікатор типу заданого поля

-   [« pg\_field\_table](function.pg-field-table.html)
    
-   [pg\_field\_type »](function.pg-field-type.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає ідентифікатор типу заданого поля
    

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

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Порядковий номер поля починаючи з нуля.

### Значення, що повертаються

OID базового типу значень поля.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

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

-   [pg\_field\_type()](function.pg-field-type.html) - Повертає ім'я типу заданого поля
-   [pg\_field\_prtlen()](function.pg-field-prtlen.html) - Повертає кількість друкованих символів
-   [pg\_field\_name()](function.pg-field-name.html) - Повертає найменування поля