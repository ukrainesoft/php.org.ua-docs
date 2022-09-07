---
navigation:
  - sqlite3.createaggregate.md: '« SQLite3::createAggregate'
  - sqlite3.createfunction.md: 'SQLite3::createFunction »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::createCollation'
---
# SQLite3::createCollation

(PHP 5> = 5.3.11, PHP 7, PHP 8)

SQLite3::createCollation — Реєструє функцію PHP для використання як функцію сортування SQL

### Опис

```methodsynopsis
public SQLite3::createCollation(string $name, callable $callback): bool
```

Реєструє функцію PHP або функцію користувача для використання як функції сортування в SQL-запитах.

### Список параметрів

`name`

Ім'я створюваної або перевизначуваної функції сортування SQL

`callback`

Ім'я PHP-функції або визначуваної користувачем функції для застосування як callback, що визначає поведінку параметрів сортування. Вона повинна приймати два значення і результат, що повертається, повинен бути такий же, як у [strcmp()](function.strcmp.md), тобто. він повинен повертати -1, 1 або 0, якщо перший рядок сортується до, після або дорівнює другому.

Функція має бути визначена як:

```methodsynopsis
collation(mixed $value1, mixed $value2): int
```

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SQLite3::createCollation()****

Реєструє PHP-функцію [strnatcmp()](function.strnatcmp.md) як послідовність сортування у базі даних SQLite3.

```php
<?php

$db = new SQLite3(":memory:");
$db->exec("CREATE TABLE test (col1 string)");
$db->exec("INSERT INTO test VALUES ('a1')");
$db->exec("INSERT INTO test VALUES ('a10')");
$db->exec("INSERT INTO test VALUES ('a2')");

$db->createCollation('NATURAL_CMP', 'strnatcmp');

$defaultSort = $db->query("SELECT col1 FROM test ORDER BY col1");
$naturalSort = $db->query("SELECT col1 FROM test ORDER BY col1 COLLATE NATURAL_CMP");

echo "сортировка по умолчанию:\n";
while ($row = $defaultSort->fetchArray()){
    echo $row['col1'], "\n";
}

echo "\nсортировка natural order:\n";
while ($row = $naturalSort->fetchArray()){
    echo $row['col1'], "\n";
}

$db->close();

?>
```

Результат виконання цього прикладу:

```
default:
a1
a10
a2

natural:
a1
a2
a10
```

### Дивіться також

-   Документація зі зіставлення SQLite: [» http://sqlite.org/datatype3.md#collation](http://sqlite.org/datatype3.md#collation)
