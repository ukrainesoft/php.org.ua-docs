Виконує запит

-   [« pg\_query\_params](function.pg-query-params.html)
    
-   [pg\_result\_error\_field »](function.pg-result-error-field.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Виконує запит
    

# пгquery

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгquery — Виконує запит

### Опис

```methodsynopsis
pg_query(PgSql\Connection $connection = ?, string $query): PgSql\Result|false
```

**пгquery()** виконує `query` до вказаної в `connection` базі даних . [pg\_query\_params()](function.pg-query-params.html) має бути кращим у більшості випадків.

У разі помилки функція повертає **`false`**, деталі помилки можна отримати за допомогою функції [pg\_last\_error()](function.pg-last-error.html)якщо з'єднання з БД не порушено.

> **Зауваження**: Незважаючи на те, що параметр `connection` може бути опущений, робити так не рекомендується, так як це може призвести до помилок, що важко перебувають у скриптах.

> **Зауваження**
> 
> Раніше ця функція називалася **пгexec()**. . **пгexec()** все ще доступна для забезпечення сумісності, але краще використовувати нове ім'я.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`query`

Вираз або вираз SQL для виконання. Якщо передано кілька виразів, вони автоматично виконуються, як одна транзакція, якщо явно не вказані команди BEGIN/COMMIT усередині виразу. Тим не менш, використовувати кілька транзакцій в одному дзвінку функції не рекомендується.

**Увага**

Строкове представлення даних користувача дуже небезпечне і часто призводить до можливості [SQL инъекции](security.database.sql-injection.html). У більшості випадків краще передавати дані користувача параметром в [pg\_query\_params()](function.pg-query-params.html), а не підставляти їх у рядок запиту.

Будь-які дані, що передаються від користувача безпосередньо в рядок запиту, повинні бути [хорошо экранированы](function.pg-escape-string.html)

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                                                                                                                         |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Повертає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше повертався ресурс ([resource](language.types.resource.html)                                  |
|        | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгquery()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_row($result)) {
  echo "Автор: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

**Приклад #2 Використання кількох виразів у **пгquery()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");

// эти выражения будут исполнены в одной транзакции

$query = "UPDATE authors SET author=UPPER(author) WHERE id=1;";
$query .= "UPDATE authors SET author=LOWER(author) WHERE id=2;";
$query .= "UPDATE authors SET author=NULL WHERE id=3;";

pg_query($conn, $query);

?>
```

### Дивіться також

-   [pg\_connect()](function.pg-connect.html) - Відкриває з'єднання з базою даних PostgreSQL
-   [pg\_pconnect()](function.pg-pconnect.html) - Відкриває постійне з'єднання із сервером PostgreSQL
-   [pg\_fetch\_array()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.html) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_num\_rows()](function.pg-num-rows.html) - Повертає кількість рядків у вибірці
-   [pg\_affected\_rows()](function.pg-affected-rows.html) - Повертає кількість порушених запитом записів (кортежів)