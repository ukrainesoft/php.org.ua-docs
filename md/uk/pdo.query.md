---
navigation:
  - pdo.prepare.md: '« PDO::prepare'
  - pdo.quote.md: 'PDO::quote »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::query'
---
# PDO::query

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.0)

PDO::query — Підготовляє та виконує вираз SQL без заповнювачів

### Опис

```methodsynopsis
public PDO::query(string $query, ?int $fetchMode = null): PDOStatement|false
```

```methodsynopsis
public PDO::query(string $query, ?int $fetchMode = PDO::FETCH_COLUMN, int $colno): PDOStatement|false
```

```methodsynopsis
public PDO::query(    string $query,    ?int $fetchMode = PDO::FETCH_CLASS,    string $classname,    array $constructorArgs): PDOStatement|false
```

```methodsynopsis
public PDO::query(string $query, ?int $fetchMode = PDO::FETCH_INTO, object $object): PDOStatement|false
```

**PDO::query()** готує та виконує вираз SQL за один виклик функції, повертаючи вираз як об'єкт [PDOStatement](class.pdostatement.md)

Якщо запит запускатиметься багаторазово, для покращення продуктивності програми має сенс цей запит один раз підготувати [PDOStatement](class.pdostatement.md) методом [PDO::prepare()](pdo.prepare.md), а потім запускати на виконання методом [PDOStatement::execute()](pdostatement.execute.md) стільки разів, скільки потрібно.

Якщо після виконання попереднього запиту ви не вибрали всі дані з результуючого набору, наступний дзвінок **PDO::query()** може зазнати невдачі. У таких випадках слід викликати метод [PDOStatement::closeCursor()](pdostatement.closecursor.md), що звільнить ресурси бази даних, зайняті попереднім об'єктом [PDOStatement](class.pdostatement.md). Після цього можна безпечно викликати **PDO::query()**

> **Зауваження**
> 
> Якщо `query` містить заповнювачі, вираз має бути підготовлено та виконано окремо з використанням методів [PDO::prepare()](pdo.prepare.md) і [PDOStatement::execute()](pdostatement.execute.md)

### Список параметрів

`query`

SQL-запит для підготовки та виконання.

Якщо SQL містить заповнювачі, замість цього слід використовувати [PDO::prepare()](pdo.prepare.md) і [PDOStatement::execute()](pdostatement.execute.md). В якості альтернативи, SQL можна підготувати вручну перед викликом **PDO::query()**, при цьому дані мають бути правильно відформатовані з використанням [PDO::quote()](pdo.quote.md)якщо драйвер підтримує це.

`fetchMode`

Режим вибірки за промовчанням для повернутого [PDOStatement](class.pdostatement.md). Має бути однією з констант [`PDO::FETCH_*`](pdo.constants.md)

Якщо цей аргумент передається функції, інші аргументи будуть оброблятися так, якби [PDOStatement::setFetchMode()](pdostatement.setfetchmode.md) був викликаний отриманого об'єкта висловлювання. Подальші аргументи залежать від вибраного режиму вибірки.

### Значення, що повертаються

Повертає об'єкт [PDOStatement](class.pdostatement.md) або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 SQL без наповнювачів може бути виконаний з використанням **PDO::query()****

```php
<?php
$sql = 'SELECT name, color, calories FROM fruit ORDER BY name';
foreach ($conn->query($sql) as $row) {
    print $row['name'] . "\t";
    print $row['color'] . "\t";
    print $row['calories'] . "\n";
}
?>
```

Результат виконання цього прикладу:

```
apple   red     150
banana  yellow  250
kiwi    brown   75
lemon   yellow  25
orange  orange  300
pear    green   150
watermelon      pink    90
```

### Дивіться також

-   [PDO::exec()](pdo.exec.md) - Виконує SQL-запит та повертає кількість порушених рядків
-   [PDO::prepare()](pdo.prepare.md) - готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.md) - Запускає підготовлений запит на виконання
