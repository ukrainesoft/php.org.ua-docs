---
navigation:
  - pdostatement.debugdumpparams.md: '« PDOStatement::debugDumpParams'
  - pdostatement.errorinfo.md: 'PDOStatement::errorInfo »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::errorCode'
---
# PDOStatement::errorCode

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDOStatement::errorCode — Отримує код SQLSTATE, пов'язаний з останньою операцією в об'єкті PDOStatement

### Опис

```methodsynopsis
public PDOStatement::errorCode(): ?string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Метод ідентичний [PDO::errorCode()](pdo.errorcode.md) за винятком того, що **PDOStatement::errorCode()** повертає коди помилок, що відбулися в результаті роботи об'єкта PDOStatement.

### Приклади

**Приклад #1 Отримання коду SQLSTATE**

```php
<?php
/* Спровоцируем ошибку -- таблицы BONES не существует */
$err = $dbh->prepare('SELECT skull FROM bones');
$err->execute();

echo "\nPDOStatement::errorCode(): ";
print $err->errorCode();
?>
```

Результат виконання цього прикладу:

```
PDOStatement::errorCode(): 42S02
```

### Дивіться також

-   [PDO::errorCode()](pdo.errorcode.md) - Повертає код SQLSTATE результату останньої операції з базою даних
-   [PDO::errorInfo()](pdo.errorinfo.md) - Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
-   [PDOStatement::errorInfo()](pdostatement.errorinfo.md) - отримання розширеної інформації про помилку, що сталася в результаті роботи об'єкта PDOStatement
