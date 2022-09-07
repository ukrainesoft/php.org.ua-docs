---
navigation:
  - pdostatement.errorcode.md: '« PDOStatement::errorCode'
  - pdostatement.execute.md: 'PDOStatement::execute »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::errorInfo'
---
# PDOStatement::errorInfo

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDOStatement::errorInfo — Отримання розширеної інформації про помилку, що сталася внаслідок роботи об'єкта PDOStatement

### Опис

```methodsynopsis
public PDOStatement::errorInfo(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**PDOStatement::errorInfo()** повертає масив з інформацією про помилку, що відповідає останній операції об'єкта PDOStatement. Масив складається як мінімум із наступних полів:

| Элемент | Информация |
| --- | --- |
|  | Код помилки SQLSTATE (п'ятисимвольний код, що складається з букв та цифр, визначений у стандарті ANSI SQL). |
|  | Код помилки повертається драйвером. |
|  | Повідомлення про помилку, яке повертається драйвером. |

### Приклади

**Приклад #1 Виведення полів errorInfo() при PDOODBC підключення до DB2**

```php
<?php
/* Спровоцируем ошибку -- таблицы BONES не существует */
$sth = $dbh->prepare('SELECT skull FROM bones');
$sth->execute();

echo "\nPDOStatement::errorInfo():\n";
$arr = $sth->errorInfo();
print_r($arr);
?>
```

Результат виконання цього прикладу:

```
PDOStatement::errorInfo():
Array
(
    [0] => 42S02
    [1] => -204
    [2] => [IBM][CLI Driver][DB2/LINUX] SQL0204N  "DANIELS.BONES" is an undefined name.  SQLSTATE=42704
)
```

### Дивіться також

-   [PDO::errorCode()](pdo.errorcode.md) - Повертає код SQLSTATE результату останньої операції з базою даних
-   [PDO::errorInfo()](pdo.errorinfo.md) - Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
-   [PDOStatement::errorCode()](pdostatement.errorcode.md) - Отримує код SQLSTATE, пов'язаний з останньою операцією в об'єкті PDOStatement
