---
navigation:
  - pdo.sqlitecreateaggregate.md: '« PDO::sqliteCreateAggregate'
  - pdo.sqlitecreatefunction.md: 'PDO::sqliteCreateFunction »'
  - index.md: PHP Manual
  - ref.pdo-sqlite.md: SQLite (PDO)
title: 'PDO::sqliteCreateCollation'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::sqliteCreateCollation

(PHP 5 >= 5.3.11, PHP 7, PHP 8)

PDO::sqliteCreateCollation — Реєстрація користувача функції сортування для використання в SQL-запитах

### Опис

```methodsynopsis
public PDO::sqliteCreateCollation(string $name, callable $callback): bool
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`name`

Ім'я функції для використання у запитах.

`callback`

Ім'я функції PHP, або певна функція для використання як функція зворотного виклику і визначальна поведінка при сортуванні. Вона повинна приймати два рядки і повертати -1 або 1, якщо перший рядок повинен розташовуватися до або після другого рядка відповідно або 0, якщо порядок не важливий.

Ця функція має бути визначена так:

```methodsynopsis
collation(string $string1, string $string2): int
```

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**PDO::sqliteCreateCollation()\*\*\*\*

```php
<?php
$db = new PDO('sqlite::memory:');
$db->exec("CREATE TABLE test (col1 string)");
$db->exec("INSERT INTO test VALUES ('a1')");
$db->exec("INSERT INTO test VALUES ('a10')");
$db->exec("INSERT INTO test VALUES ('a2')");

$db->sqliteCreateCollation('NATURAL_CMP', 'strnatcmp');
foreach ($db->query("SELECT col1 FROM test ORDER BY col1") as $row) {
  echo $row['col1'] . "\n";
}
echo "\n";
foreach ($db->query("SELECT col1 FROM test ORDER BY col1 COLLATE NATURAL_CMP") as $row) {
  echo $row['col1'] . "\n";
}
?>
```

Результат виконання наведеного прикладу:

```
a1
a10
a2

a1
a2
a10
```
