---
navigation:
  - function.mysql-fetch-object.md: « mysqlfetchobject
  - function.mysql-field-flags.md: mysqlfieldflags »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlfetchrow
---
# mysqlfetchrow

(PHP 4, PHP 5)

mysqlfetchrow — Обробляє ряд результату запиту та повертає масив із числовими індексами

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlifetchrow()](mysqli-result.fetch-row.md)
-   [PDOStatement::fetch(PDO::FETCHNUM)](pdostatement.fetch.md)

### Опис

```methodsynopsis
mysql_fetch_row(resource $result): array
```

Повертає масив з числовими індексами, що містить дані обробленого ряду, і зсуває внутрішній покажчик результату вперед.

### Список параметрів

`result`

оброблюваний [результат запроса](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysqlquery()](function.mysql-query.md)

### Значення, що повертаються

Повертає масив рядків з числовими індексами, що містить дані обробленого ряду, або \*\*`false`\*\*якщо рядів не залишилося.

**mysqlfetchrow()** обробляє один ряд результату, який посилається переданий покажчик. Ряд повертається як масиву. Кожна колонка розташовується в наступному осередку масиву, починаючи з нульового індексу

### Приклади

**Приклад #1 Отримання одного ряду за допомогою **mysqlfetchrow()****

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка запроса: ' . mysql_error();
    exit;
}
$row = mysql_fetch_row($result);

echo $row[0]; // 42
echo $row[1]; // email
?>
```

### Примітки

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Дивіться також

-   [mysqlfetcharray()](function.mysql-fetch-array.md) - Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysqlfetchassoc()](function.mysql-fetch-assoc.md) - Повертає ряд результату запиту як асоціативний масив.
-   [mysqlfetchobject()](function.mysql-fetch-object.md) - обробляє ряд результату запиту та повертає об'єкт
-   [mysqldataseek()](function.mysql-data-seek.md) - Переміщує внутрішній покажчик у результаті запиту
-   [mysqlfetchlengths()](function.mysql-fetch-lengths.md) - Повертає довжину кожного поля в результаті
-   [mysqlresult()](function.mysql-result.md) - Повертає дані результату запиту
