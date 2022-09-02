---
navigation:
  - sqlite3stmt.execute.md: '« SQLite3Stmt::execute'
  - sqlite3stmt.paramcount.md: 'SQLite3Stmt::paramCount »'
  - index.md: PHP Manual
  - class.sqlite3stmt.md: SQLite3Stmt
title: 'SQLite3Stmt::getSQL'
---
# SQLite3Stmt::getSQL

(PHP 7> = 7.4.0, PHP 8)

SQLite3Stmt::getSQL — Отримати SQL-запит у вигляді рядка із запиту

### Опис

```methodsynopsis
public SQLite3Stmt::getSQL(bool $expand = false): string|false
```

Повертає строкове подання SQL-запиту для підготовленого запиту. Якщо параметр `expand` заданий як **`false`**, буде повернуто не модифікований SQL. Якщо ж `expand` заданий як **`true`**, всі параметри запиту будуть замінені на конкретні значення, або на `NULL`якщо значення ще не були прив'язані.

### Список параметрів

`expand`

Чи замінювати у SQL-запиті, що повертається, параметри на конкретні значення . **`true`** підтримується лише з libsqlite 3.14.

### Значення, що повертаються

Повертає SQL-запит із підготовленого запиту або **`false`** у разі виникнення помилки.

### Помилки

Якщо `expand` заданий як **`true`**, але версія libsqlite нижче 3.14, буде викликана помилка рівня **`E_WARNING`** або викинуто виняток [Exception](class.exception.md), в залежності від налаштувань [SQLite3::enableExceptions()](sqlite3.enableexceptions.md)

### Приклади

**Приклад #1 Отримання розширеного SQL-запиту**

```php
<?php
$db = new SQLite3(':memory:');
$stmt = $db->prepare("SELECT :a, ?, :c");
$stmt->bindValue(':a', 'foo');
$answer = 42;
$stmt->bindParam(2, $answer);
var_dump($stmt->getSQL(true));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(24) "SELECT 'foo', '42', NULL"
```
