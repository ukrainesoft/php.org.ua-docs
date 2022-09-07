---
navigation:
  - class.sqlite3.md: « SQLite3
  - sqlite3.busytimeout.md: 'SQLite3::busyTimeout »'
  - index.md: PHP Manual
  - class.sqlite3.md: SQLite3
title: 'SQLite3::backup'
---
# SQLite3::backup

(PHP 7> = 7.4.0, PHP 8)

SQLite3::backup — Резервне копіювання однієї бази даних до іншої

### Опис

```methodsynopsis
public SQLite3::backup(SQLite3 $destination, string $sourceDatabase = "main", string $destinationDatabase = "main"): bool
```

**SQLite3::backup()** копіює вміст однієї бази на іншу, перезаписуючи вміст цільової бази. Це корисно як для створення резервних копій, так і для копіювання in-memory баз у файл або з файлу.

**Підказка**

Починаючи з SQLite 3.27.0 (07.02.2019), також можна використовувати конструкцію `VACUUM INTO 'file.db';` для резервного копіювання бази даних у новий файл.

### Список параметрів

`destination`

З'єднання з базою, відкрите за допомогою [SQLite3::open()](sqlite3.open.md)

`sourceDatabase`

Назва бази даних. Для головної бази `"main"`, для тимчасової `"temp"`, або ім'я, задане після ключового слова `AS` у виразі `ATTACH` для приєднаних баз.

`destinationDatabase`

Аналогічно `sourceDatabase` але для `destinationDatabase`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення резервної копії існуючої бази**

```php
<?php
// $conn is a connection to an already opened sqlite3 database

$backup = new SQLite3('backup.sqlite');
$conn->backup($backup);
?>
```
