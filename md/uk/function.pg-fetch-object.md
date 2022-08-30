Вибирає рядок результату запиту та повертає дані у вигляді об'єкта

-   [« pgfetchassoc](function.pg-fetch-assoc.html)
    
-   [пгfetchresult »](function.pg-fetch-result.html)
    
-   [PHP Manual](index.md)
    
-   [Функции PostgreSQL](ref.pgsql.md)
    
-   Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
    

# пгfetchobject

(PHP 4, PHP 5, PHP 7, PHP 8)

пгfetchobject — Виберіть рядок результату запиту та повертає дані у вигляді об'єкта.

### Опис

```methodsynopsis
pg_fetch_object(    PgSql\Result $result,    ?int $row = null,    string $class = "stdClass",    array $constructor_args = []): object|false
```

**пгfetchobject()** повертає об'єкт, властивості якого відповідають іменам полів вибірки. Також функція може створити екземпляр конкретного класу та передати параметри його конструктору.

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

За швидкістю функція ідентична [пгfetcharray()](function.pg-fetch-array.html) і трохи повільніше [пгfetchrow()](function.pg-fetch-row.html) (Різниця незначна).

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

`class`

Ім'я класу об'єкта, що створюється і повертається. Якщо не встановлено, функція створить екземпляр класу **stdClass**

`constructor_args`

Необов'язковий аргумент. Масив (array) параметрів передачі в конструктор створюваного об'єкта (`class`

### Значення, що повертаються

Об'єкт (object), імена та значення властивостей якого відповідають іменам та значенням полів результату запиту. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, коли `row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Описание                                                                                                                                         |
|--------|--------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгfetchobject()****

```php
<?php

$database = "store";

$db_conn = pg_connect("host=localhost port=5432 dbname=$database");
if (!$db_conn) {
  echo "Невозможно соединиться с базой postgres $database\n";
  exit;
}

$qu = pg_query($db_conn, "SELECT * FROM books ORDER BY author");


while ($data = pg_fetch_object($qu)) {
  echo $data->author . " (";
  echo $data->year . "): ";
  echo $data->title . "<br />";
}

pg_free_result($qu);
pg_close($db_conn);

?>
```

### Дивіться також

-   [пгquery()](function.pg-query.html) - Виконує запит
-   [пгfetcharray()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву
-   [пгfetchassoc()](function.pg-fetch-assoc.html) - Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [пгfetchrow()](function.pg-fetch-row.html) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfetchresult()](function.pg-fetch-result.html) - Повертає запис із результату запиту