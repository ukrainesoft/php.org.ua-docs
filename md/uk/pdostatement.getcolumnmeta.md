---
navigation:
  - pdostatement.getattribute.md: '« PDOStatement::getAttribute'
  - pdostatement.getiterator.md: 'PDOStatement::getIterator »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::getColumnMeta'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::getColumnMeta

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.0)

PDOStatement::getColumnMeta — Повертає метадані стовпця у результуючій таблиці

### Опис

```methodsynopsis
public PDOStatement::getColumnMeta(int $column): array|false
```

Повертає метадані стовпця результуючої таблиці як асоціативного масиву. Індексація стовпців починається із 0.

**Увага**

Деякі драйвери PDO можуть не виконувати функцію \*\*PDOStatement::getColumnMeta()\*\*оскільки вона є необов'язковою. Однак усі [драйвери PDO](pdo.drivers.md), зазначені в посібнику, реалізують цю функцію.

### Список параметрів

`column`

Індекс (починаючи з 0) стовпця результуючого набору.

### Значення, що повертаються

Повертає асоціативний масив, що містить такі значення метаданих:

**Метадані стовпця**

| Имя | Значение |
| --- | --- |
| `native_type` | Внутрішній тип PHP, який використовується для представлення значення стовпця. |
| `driver:decl_type` | Тип SQL, що використовується для представлення значення стовпця у базі даних. Якщо значення стовпця результуючої таблиці повернуто з функції, **PDOStatement::getColumnMeta()** не визначатиме цей тип. |
| `flags` | Будь-які прапори, встановлені для стовпчика. |
| `name` | Ім'я цього стовпця, яке повертається базою даних. |
| `table` | Ім'я таблиці цього стовпця, яке повертається базою даних. |
| `len` | Розмір поля стовпця. Як правило, для типів, відмінних від чисел з плаваючою точкою, це значення дорівнює `-1` |
| `precision` | Числова точність цього стовпця. Як правило, для типів, відмінних від чисел з плаваючою точкою, це значення дорівнює |
| `pdo_type` | Тип PDO значення стовпця у вигляді однієї з констант [`PDO::PARAM_*`](pdo.constants.md) |

Повертає **`false`** у випадках, коли зазначеного стовпця немає в результуючій таблиці, а також якщо не існує результуючого набору.

### Приклади

**Приклад #1 Вилучення метаданих стовпця**

У наступному прикладі показано результати вилучення метаданих одного стовпця, згенерованого функцією COUNT драйвера PDO\_SQLITE.

```php
<?php
$select = $DB->query('SELECT COUNT(*) FROM fruit');
$meta = $select->getColumnMeta(0);
var_dump($meta);
?>
```

Результат виконання наведеного прикладу:

```
array(6) {
  ["native_type"]=>
  string(7) "integer"
  ["flags"]=>
  array(0) {
  }
  ["name"]=>
  string(8) "COUNT(*)"
  ["len"]=>
  int(-1)
  ["precision"]=>
  int(0)
  ["pdo_type"]=>
  int(2)
}
```

### Дивіться також

-   [PDOStatement::columnCount()](pdostatement.columncount.md) \- Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::rowCount()](pdostatement.rowcount.md) \- Повертає кількість рядків, порушених останнім SQL-запитом
