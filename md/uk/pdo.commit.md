---
navigation:
  - pdo.begintransaction.md: '« PDO::beginTransaction'
  - pdo.construct.md: 'PDO::\_\_construct »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::commit'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::commit

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDO::commit - Фіксує транзакцію

### Опис

```methodsynopsis
public PDO::commit(): bool
```

Фіксує транзакцію, повертаючи з'єднання з базою даних у режим автоматичної фіксації доти, доки наступний виклик [PDO::beginTransaction()](pdo.begintransaction.md) не розпочне нову транзакцію.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Викликає виняток [PDOException](class.pdoexception.md)якщо немає активної транзакції.

> **Зауваження**: Виняток буде викликано, навіть якщо атрибут **`PDO::ATTR_ERRMODE`** не виставлений у **`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Фіксація звичайної транзакції**

```php
<?php
/* Начало транзакции, отключение автоматической фиксации */
$dbh->beginTransaction();

/* Вставка множества записей по принципу "все или ничего" */
$sql = 'INSERT INTO fruit
    (name, colour, calories)
    VALUES (?, ?, ?)';

$sth = $dbh->prepare($sql);

foreach ($fruits as $fruit) {
    $sth->execute(array(
        $fruit->name,
        $fruit->colour,
        $fruit->calories,
    ));
}

/* Фиксация изменений */
$dbh->commit();

/* Соединение с базой данных снова в режиме автоматической фиксации */
?>
```

**Приклад #2 Фіксація DDL-транзакції**

```php
<?php
/* Начало транзакции, отключение автоматической фиксации */
$dbh->beginTransaction();

/* Изменение схемы базы данных */
$sth = $dbh->exec("DROP TABLE fruit");

/* Фиксация изменений */
$dbh->commit();

/* Соединение с базой данных снова в режиме автоматической фиксации */
?>
```

> **Зауваження**: Не всі бази даних дозволяють транзакціям працювати з DDL-виразами: в деяких генеруються помилки, тоді як в інших (включаючи MySQL) транзакція автоматично фіксується після першого DDL-виразу, що зустрівся.

### Дивіться також

-   [PDO::beginTransaction()](pdo.begintransaction.md) \- Ініціалізація транзакції
-   [PDO::rollBack()](pdo.rollback.md) \- Відкат транзакції
-   [Транзакції та автоматична фіксація](pdo.transactions.md)
