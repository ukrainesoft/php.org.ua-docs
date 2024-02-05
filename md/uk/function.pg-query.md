---
navigation:
  - function.pg-query-params.md: « pg\_query\_params
  - function.pg-result-error-field.md: pg\_result\_error\_field »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_query

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_query — Виконує запит

### Опис

```methodsynopsis
pg_query(PgSql\Connection $connection = ?, string $query): PgSql\Result|false
```

**pg\_query()** виконує `query` до вказаної в `connection` базі даних . [pg\_query\_params()](function.pg-query-params.md) має бути кращим у більшості випадків.

В случае возникновения ошибки функция возвращает\*\*`false`\*\*, деталі помилки можна отримати за допомогою функції [pg\_last\_error()](function.pg-last-error.md)якщо з'єднання з БД не порушено.

> **Зауваження**: Несмотря на то, что параметр`connection` може бути опущений, робити так не рекомендується, так як це може призвести до помилок, що важко перебувають у скриптах.

> **Зауваження** :
> 
> Раніше ця функція називалася **pg\_exec()**. . **pg\_exec()** все ще доступна для забезпечення сумісності, але краще використовувати нове ім'я.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`query`

Вираз або вираз SQL для виконання. Якщо передано кілька виразів, вони автоматично виконуються, як одна транзакція, якщо явно не вказані команди BEGIN/COMMIT усередині виразу. Тим не менш, використовувати кілька транзакцій в одному дзвінку функції не рекомендується.

**Увага**

Строкове представлення даних користувача дуже небезпечне і часто призводить до можливості [SQL ін'єкції](security.database.sql-injection.md). У більшості випадків краще передавати дані користувача параметром в [pg\_query\_params()](function.pg-query-params.md), а не підставляти їх у рядок запиту.

Будь-які дані, що передаються від користувача безпосередньо в рядок запиту, повинні бути [добре екрановані](function.pg-escape-string.md)

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_query()\*\*\*\*

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

**Приклад #2 Використання кількох виразів у **pg\_query()****

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

-   [pg\_connect()](function.pg-connect.md) \- Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.md) \- Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_num\_rows()](function.pg-num-rows.md) \- Повертає кількість рядків у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.md) \- Повертає кількість порушених запитом записів (кортежів)
