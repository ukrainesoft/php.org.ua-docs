---
navigation:
  - pdostatement.setattribute.md: '« PDOStatement::setAttribute'
  - class.pdorow.md: PDORow »
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::setFetchMode'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::setFetchMode

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.0)

PDOStatement::setFetchMode — Встановлює режим вибірки за промовчанням для об'єкта запиту

### Опис

```methodsynopsis
public PDOStatement::setFetchMode(int $mode): bool
```

```methodsynopsis
public PDOStatement::setFetchMode(int $mode = PDO::FETCH_COLUMN, int $colno): bool
```

```methodsynopsis
public PDOStatement::setFetchMode(int $mode = PDO::FETCH_CLASS, string $class, ?array $constructorArgs = null): bool
```

```methodsynopsis
public PDOStatement::setFetchMode(int $mode = PDO::FETCH_INTO, object $object): bool
```

### Список параметрів

`mode`

Режим вибірки можна задавати лише однією з констант [**`PDO::FETCH_*`**](pdo.constants.md)

`colno`

Номер стовпця.

`class`

Назва класу.

`constructorArgs`

Аргументи конструктора класу.

`object`

Об'єкт.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Зміна режиму вибірки**

В следующем Прикладе показано, как метод**PDOStatement::setFetchMode()** змінює режим вибірки за промовчанням для об'єкта PDOStatement.

```php
<?php
$stmt = $dbh->query('SELECT name, colour, calories FROM fruit');
$stmt->setFetchMode(PDO::FETCH_NUM);
foreach ($stmt as $row) {
    print $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
}
```

Результат виконання наведеного прикладу:

```
apple   red     150
banana  yellow  250
orange  orange  300
kiwi    brown   75
lemon   yellow  25
pear    green   150
```
