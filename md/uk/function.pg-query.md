---
navigation:
  - function.pg-query-params.md: « pgqueryparams
  - function.pg-result-error-field.md: пгresulterrorfield »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгquery
---
# пгquery

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгquery — Виконує запит

### Опис

```methodsynopsis
pg_query(PgSql\Connection $connection = ?, string $query): PgSql\Result|false
```

**пгquery()** виконує `query` до вказаної в `connection` базі даних . [пгqueryparams()](function.pg-query-params.md) має бути кращим у більшості випадків.

У разі помилки функція повертає **`false`**, деталі помилки можна отримати за допомогою функції [пгlasterror()](function.pg-last-error.md)якщо з'єднання з БД не порушено.

> **Зауваження**: Незважаючи на те, що параметр `connection` може бути опущений, робити так не рекомендується, так як це може призвести до помилок, що важко перебувають у скриптах.

> **Зауваження**
> 
> Раніше ця функція називалася **пгexec()**. . **пгexec()** все ще доступна для забезпечення сумісності, але краще використовувати нове ім'я.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`query`

Вираз або вираз SQL для виконання. Якщо передано кілька виразів, вони автоматично виконуються, як одна транзакція, якщо явно не вказані команди BEGIN/COMMIT усередині виразу. Тим не менш, використовувати кілька транзакцій в одному дзвінку функції не рекомендується.

**Увага**

Строкове представлення даних користувача дуже небезпечне і часто призводить до можливості [SQL ін'єкції](security.database.sql-injection.md). У більшості випадків краще передавати дані користувача параметром в [пгqueryparams()](function.pg-query-params.md), а не підставляти їх у рядок запиту.

Будь-які дані, що передаються від користувача безпосередньо в рядок запиту, повинні бути [добре екрановані](function.pg-escape-string.md)

### Значення, що повертаються

Екземпляр [PgSqlResult](class.pgsql-result.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSqlResult](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгquery()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_row($result)) {
  echo "Автор: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

**Приклад #2 Використання кількох виразів у **пгquery()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");

// эти выражения будут исполнены в одной транзакции

$query = "UPDATE authors SET author=UPPER(author) WHERE id=1;";
$query .= "UPDATE authors SET author=LOWER(author) WHERE id=2;";
$query .= "UPDATE authors SET author=NULL WHERE id=3;";

pg_query($conn, $query);

?>
```

### Дивіться також

-   [пгconnect()](function.pg-connect.md) - Відкриває з'єднання з базою даних PostgreSQL
-   [пгpconnect()](function.pg-pconnect.md) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [пгfetcharray()](function.pg-fetch-array.md) - Повертає рядок результату у вигляді масиву
-   [пгfetchobject()](function.pg-fetch-object.md) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгnumrows()](function.pg-num-rows.md) - Повертає кількість рядків у вибірці
-   [пгaffectedrows()](function.pg-affected-rows.md) - Повертає кількість порушених запитом записів (кортежів)
