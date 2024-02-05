---
navigation:
  - function.mysql-fetch-object.md: « mysql\_fetch\_object
  - function.mysql-field-flags.md: mysql\_field\_flags »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_fetch\_row
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_fetch\_row

(PHP 4, PHP 5)

mysql\_fetch\_row — Обробляє ряд результату запиту та повертає масив із числовими індексами

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_fetch\_row()](mysqli-result.fetch-row.md)
-   [PDOStatement::fetch()](pdostatement.fetch.md)с параметром`mode`заданим як\*\*`PDO::FETCH_NUM`\*\*

### Опис

```methodsynopsis
mysql_fetch_row(resource $result): array
```

Повертає масив з числовими індексами, що містить дані обробленого ряду, і зсуває внутрішній покажчик результату вперед.

### Список параметрів

`result`

оброблюваний [результат запиту](language.types.resource.md). Цей результат можна отримати за допомогою функції [mysql\_query()](function.mysql-query.md)

### Значення, що повертаються

Повертає масив рядків з числовими індексами, що містить дані обробленого ряду, або \*\*`false`\*\*якщо рядів не залишилося.

**mysql\_fetch\_row()** обробляє один ряд результату, який посилається переданий покажчик. Ряд повертається як масиву. Кожна колонка розташовується в наступному осередку масиву, починаючи з нульового індексу

### Приклади

**Пример #1 Получение одного ряда с помощью**mysql\_fetch\_row()\*\*\*\*

```php
<?php
$result = mysql_query("SELECT id,email FROM people WHERE id = '42'");
if (!$result) {
    echo 'Ошибка запроса: ' . mysql_error();
    exit;
}
$row = mysql_fetch_row($result);

echo $row[0]; // 42
echo $row[1]; // email
?>
```

### Примітки

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Дивіться також

-   [mysql\_fetch\_array()](function.mysql-fetch-array.md) \- Обробляє ряд результатів запиту, повертаючи асоціативний масив, чисельний масив або обидва
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) \- Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_fetch\_object()](function.mysql-fetch-object.md) \- обробляє ряд результату запиту та повертає об'єкт
-   [mysql\_data\_seek()](function.mysql-data-seek.md) \- Переміщує внутрішній покажчик у результаті запиту
-   [mysql\_fetch\_lengths()](function.mysql-fetch-lengths.md) \- Повертає довжину кожного поля в результаті
-   [mysql\_result()](function.mysql-result.md) \- Повертає дані результату запиту
