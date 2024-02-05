---
navigation:
  - mysql-xdevapi-rowresult.fetchone.md: '« RowResult::fetchOne'
  - mysql-xdevapi-rowresult.getcolumnnames.md: 'RowResult::getColumnNames »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-rowresult.md: mysql\_xdevapi\\RowResult
title: 'RowResult::getColumnsCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RowResult::getColumnsCount

(No version information available, might only be in Git)

RowResult::getColumnsCount — Отримує кількість стовпців

### Опис

```methodsynopsis
public mysql_xdevapi\RowResult::getColumnsCount(): int
```

Отримує кількість стовпців, які є у наборі результатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість стовпців; 0 якщо їх немає

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.14 | Метод перейменований з getColumnCount() на getColumnsCount(). |

### Приклади

**Пример #1 Пример использования**mysql\_xdevapi\\RowResult::getColumnsCount()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE addressbook")->execute();
$session->sql("CREATE DATABASE foo")->execute();
$session->sql("CREATE TABLE foo.test_table(x int)")->execute();
$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();

$sql = $session->sql("SELECT * from addressbook.names")->execute();

echo $sql->getColumnsCount();
```

Висновок наведеного прикладу буде схожим на:

```
2
```
