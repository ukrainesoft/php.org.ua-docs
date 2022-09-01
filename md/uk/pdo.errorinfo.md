---
navigation:
  - pdo.errorcode.html: '« PDO::errorCode'
  - pdo.exec.html: 'PDO::exec »'
  - index.html: PHP Manual
  - class.pdo.html: PDO
title: 'PDO::errorInfo'
---
# PDO::errorInfo

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDO::errorInfo — Отримує розширену інформацію про помилку, що сталася під час останнього звернення до бази даних

### Опис

```methodsynopsis
public PDO::errorInfo(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**PDO::errorInfo()** повертає масив з інформацією про помилку, що сталася під час виконання останньої операції з базою даних. Масив містить щонайменше такі поля:

| Элемент | Информация |
| --- | --- |
|  | Код помилки SQLSTATE (п'ятисимвольний ідентифікатор, визначений у стандарті ANSI SQL). |
|  | Код помилки заданий драйвером. |
|  | Повідомлення про помилку, задане драйвером |

> **Зауваження**
> 
> Якщо не встановлено SQLSTATE код або драйвер не повідомив про помилку, то елементи наступні за нульовим будуть мати значення **`null`**

**PDO::errorInfo()** видає інформацію про помилку тільки для операцій, що здійснюються з базою даних безпосередньо з PDO. Якщо створити об'єкт PDOStatement методами [PDO::prepare()](pdo.prepare.html) або [PDO::query()](pdo.query.html), і викликати помилку його методами, **PDO::errorInfo()** цю помилку не відобразить. Вам потрібно викликати [PDOStatement::errorInfo()](pdostatement.errorinfo.html), щоб отримати інформацію про помилки для операції, що виконується на певному об'єкті PDOStatement.

### Приклади

**Приклад #1 Виведення полів масиву errorInfo() для PDOODBC підключення до бази даних DB2**

```php
<?php
/* Спровоцируем синтаксическую ошибку SQL */
$stmt = $dbh->prepare('bogus sql');
if (!$stmt) {
    echo "\nPDO::errorInfo():\n";
    print_r($dbh->errorInfo());
}
?>
```

Результат виконання цього прикладу:

```
PDO::errorInfo():
Array
(
    [0] => HY000
    [1] => 1
    [2] => near "bogus": syntax error
)
```

### Дивіться також

-   [PDO::errorCode()](pdo.errorcode.html) - Повертає код SQLSTATE результату останньої операції з базою даних
-   [PDOStatement::errorCode()](pdostatement.errorcode.html) - Отримує код SQLSTATE, пов'язаний з останньою операцією в об'єкті PDOStatement
-   [PDOStatement::errorInfo()](pdostatement.errorinfo.html) - отримання розширеної інформації про помилку, що сталася в результаті роботи об'єкта PDOStatement
