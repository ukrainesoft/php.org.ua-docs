Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив

-   [« pg\_execute](function.pg-execute.html)
    
-   [pg\_fetch\_all »](function.pg-fetch-all.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив
    

# пгfetchallcolumns

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгfetchallcolumns — Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив

### Опис

```methodsynopsis
pg_fetch_all_columns(PgSql\Result $result, int $field = 0): array
```

**пгfetchallcolumns()** повертає масив, що містить усі записи однієї колонки екземпляра [PgSql\\Result](class.pgsql-result.html)

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.html), що повертається функціями [pg\_query()](function.pg-query.html) [pg\_query\_params()](function.pg-query-params.html) або [pg\_execute()](function.pg-execute.html) (між іншим).

`field`

Номер колонки. Якщо параметр не заданий, буде оброблено першу (нульову) колонку.

### Значення, що повертаються

Масив значень стовпчика результату запиту.

### список змін

| Версия | Описание                                                                                                                                             |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгfetchallcolumns()****

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT title, name, address FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

// Получить массив имён всех авторов
$arr = pg_fetch_all_columns($result, 1);

var_dump($arr);

?>
```

### Дивіться також

-   [pg\_fetch\_all()](function.pg-fetch-all.html) - Вибирає всі дані з результату запиту та поміщає їх у масив