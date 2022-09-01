---
navigation:
  - pdo.construct.md: '« PDO::construct'
  - pdo.errorinfo.md: 'PDO::errorInfo »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::errorCode'
---
# PDO::errorCode

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDO::errorCode — Повертає код SQLSTATE результату останньої операції з базою даних

### Опис

```methodsynopsis
public PDO::errorCode(): ?string
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає SQLSTATE – п'ятисимвольний ідентифікатор, визначений у стандарті ANSI SQL-92. Перші два символи SQLSTATE відповідають за клас помилки, а наступні три визначають її підклас. Клас помилок 01 означає попередження, якому супроводжує код SQL, що повертається.SUCCESSWITHINFO. Класи, відмінні від 01, крім 'IM', означають помилки виконання запитів до бази даних. Клас 'IM' свідчить про помилки та попередження, які викликані самореалізацією PDO (або, можливо, ODBC, якщо використовується драйвер ODBC). Значення підкласу '000' у будь-якому класі означає, що підклас для цього SQLSTATE відсутній.

**PDO::errorCode()** видає код помилки лише операцій, здійснюваних з базою даних безпосередньо з PDO. Якщо створити об'єкт PDOStatement методами [PDO::prepare()](pdo.prepare.md) або [PDO::query()](pdo.query.md), і викликати помилку його методами, **PDO::errorCode()** цю помилку не відобразить. Вам потрібно викликати [PDOStatement::errorCode()](pdostatement.errorcode.md), щоб отримати код помилки для операції, що виконується на певному об'єкті PDOStatement.

Повертає \*\*`null`\*\*якщо жодних операцій над базою даних засобами PDO-об'єкта не проводилося.

### Приклади

**Приклад #1 Отримання коду SQLSTATE**

```php
<?php
/* Спровоцируем ошибку -- таблицы BONES не существует */
$dbh->exec("INSERT INTO bones(skull) VALUES ('lucy')");

echo "\nPDO::errorCode(): ", $dbh->errorCode();
?>
```

Результат виконання цього прикладу:

```
PDO::errorCode(): 42S02
```

### Дивіться також

-   [PDO::errorInfo()](pdo.errorinfo.md) - Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних
-   [PDOStatement::errorCode()](pdostatement.errorcode.md) - Отримує код SQLSTATE, пов'язаний з останньою операцією в об'єкті PDOStatement
-   [PDOStatement::errorInfo()](pdostatement.errorinfo.md) - отримання розширеної інформації про помилку, що сталася в результаті роботи об'єкта PDOStatement
