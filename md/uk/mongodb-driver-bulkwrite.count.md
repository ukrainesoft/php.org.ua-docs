- [« MongoDB\Driver\BulkWrite::\_\_construct](mongodb-driver-bulkwrite.construct.md)
- [MongoDB\Driver\BulkWrite::delete »](mongodb-driver-bulkwrite.delete.md)

- [PHP Manual](index.md)
- [MongoDB\Driver\BulkWrite](class.mongodb-driver-bulkwrite.md)
- підраховує кількість операцій запису в порції

# MongoDB\Driver\BulkWrite::count

(mongodb \>=1.0.0)

MongoDB\Driver\BulkWrite::count - Підраховує кількість операцій
записи у порції

### Опис

public **MongoDB\Driver\BulkWrite::count**(): int

Повертає кількість операцій запису, доданих до об'єкту
[MongoDB\Driver\BulkWrite](class.mongodb-driver-bulkwrite.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість операцій запису, доданих до об'єкту
[MongoDB\Driver\BulkWrite](class.mongodb-driver-bulkwrite.md).

### Помилки

- При помилці парсингу аргумент кидає виняток
[MongoDB\Driver\Exception\InvalidArgumentException](class.mongodb-driver-exception-invalidargumentexception.md).

### Список змін

| Версія             | Опис                                                                                                                                                                                                                                              |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| PECL mongodb 1.2.0 | Повертає кількість операцій запису, доданих до об'єкта [MongoDB\Driver\BulkWrite](class.mongodb-driver-bulkwrite.md). У ранніх версіях поверталося передбачуване кількість звернень клієнта до сервера, необхідні виконання всіх операцій записи. |

### Приклади

**Приклад #1 Приклад використання **MongoDB\Driver\BulkWrite::count()****

` <?php$bulk = new MongoDB\Driver\BulkWrite;$bulk->insert(['_id' => 1, 'x' => 1]);$bulk->insert(['_id' => 2 , 'x' => 2]);$bulk->update(['x' => 2], ['$set' => ['x' => 1]]);$bulk->delete([ 'x' => 1]);var_dump(count($bulk));?> `

Результат виконання цього прикладу:

int(4)
