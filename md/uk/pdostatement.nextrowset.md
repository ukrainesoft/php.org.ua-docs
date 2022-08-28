Перехід до наступного набору рядків через запит

-   [« PDOStatement::getIterator](pdostatement.getiterator.html)
    
-   [PDOStatement::rowCount »](pdostatement.rowcount.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Перехід до наступного набору рядків через запит
    

# PDOStatement::nextRowset

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.0)

PDOStatement::nextRowset — Перехід до наступного набору рядків через запит

### Опис

```methodsynopsis
public PDOStatement::nextRowset(): bool
```

Деякі СУБД підтримують процедури, що зберігаються, які повертають більше одного набору рядків (його ще називають результуючим набором) . **PDOStatement::nextRowset()** дозволяє отримати доступ до другого та подальших наборів, що відповідають об'єкту PDOStatement. Різні набори рядків можуть мати різну кількість стовпців.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Вилучення даних з декількох наборів рядків, повернутих процедурою, що зберігається.**

У наступному прикладі показано, як викликати процедуру, що зберігається. `MULTIPLE_ROWSETS`яка повертає три набори рядків. Ми викликаємо **PDOStatement::nextRowset()** у циклі [do-while](control-structures.do.while.html)поки він не поверне **`false`** і завершить цикл, коли не буде доступних результуючих наборів.

```php
<?php
$sql = 'CALL multiple_rowsets()';
$stmt = $conn->query($sql);
$i = 1;
do {
    $rowset = $stmt->fetchAll(PDO::FETCH_NUM);
    if ($rowset) {
        printResultSet($rowset, $i);
    }
    $i++;
} while ($stmt->nextRowset());

function printResultSet(&$rowset, $i) {
    print "Результирующий набор $i:\n";
    foreach ($rowset as $row) {
        foreach ($row as $col) {
            print $col . "\t";
        }
        print "\n";
    }
    print "\n";
}
?>
```

Результат виконання цього прикладу:

```
Результирующий набор 1:
apple    red
banana   yellow

Результирующий набор 2:
orange   orange    150
banana   yellow    175

Результирующий набор 3:
lime     green
apple    red
banana   yellow
```

### Дивіться також

-   [PDOStatement::columnCount()](pdostatement.columncount.html) - Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::execute()](pdostatement.execute.html) - Запускає підготовлений запит на виконання
-   [PDOStatement::getColumnMeta()](pdostatement.getcolumnmeta.html) - Повертає метадані стовпця у результуючій таблиці
-   [PDO::query()](pdo.query.html) - готує та виконує вираз SQL без заповнювачів