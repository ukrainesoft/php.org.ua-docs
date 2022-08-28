Повертає назву або ідентифікатор таблиці, що містить задане поле

-   [« pg\_field\_size](function.pg-field-size.html)
    
-   [pg\_field\_type\_oid »](function.pg-field-type-oid.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Повертає назву або ідентифікатор таблиці, що містить задане поле
    

# пгfieldtable

(PHP 5> = 5.2.0, PHP 7, PHP 8)

пгfieldtable — Повертає назву або ідентифікатор таблиці, що містить задане поле

### Опис

```methodsynopsis
pg_field_table(PgSql\Result $result, int $field, bool $oid_only = false): string|int|false
```

**пгfieldtable()** повертає ім'я таблиці, до якої належить задане поле. Якщо як аргумент `oid_only` передається **`true`**, функція поверне oid-ідентифікатор таблиці

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Порядковий номер поля результату запиту з нуля.

`oid_only`

За замовчуванням функція повертає назву таблиці, що містить поле. Якщо параметр `oid_only` дорівнює **`true`**то функція поверне oid таблиці.

### Значення, що повертаються

При успішному завершенні назва таблиці або її oid або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Отримання інформації про поле вибірки**

```php
<?php
$dbconn = pg_connect("dbname=publisher") or die("Не удалось соединиться с базой");

$res = pg_query($dbconn, "SELECT bar FROM foo");

echo pg_field_table($res, 0);
echo pg_field_table($res, 0, true);

$res = pg_query($dbconn, "SELECT version()");
var_dump(pg_field_table($res, 0));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
foo
14379580

bool(false)
```

### Примітки

> **Зауваження**
> 
> Повернення oid таблиці значно швидше, ніж назви, оскільки визначення назви вимагає виконання додаткового запиту до системної таблиці бази даних.

### Дивіться також

-   [pg\_field\_name()](function.pg-field-name.html) - Повертає найменування поля
-   [pg\_field\_type()](function.pg-field-type.html) - Повертає ім'я типу заданого поля