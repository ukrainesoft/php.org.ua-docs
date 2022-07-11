- [« RowResult::\_\_construct](mysql-xdevapi-rowresult.construct.md)
- [RowResult::fetchOne »](mysql-xdevapi-rowresult.fetchone.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\RowResult](class.mysql-xdevapi-rowresult.md)
- Отримує всі рядки з результату

# RowResult::fetchAll

(No version information available, might only be in Git)

RowResult::fetchAll — Отримує усі рядки з результату

### Опис

public **mysql_xdevapi\RowResult::fetchAll**(): array

Витягує всі рядки з набору результатів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Числовий масив із усіма результатами запиту; кожен результат
є асоціативний масив. Повертається порожній масив,
якщо рядків немає.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\RowResult::fetchAll()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE addressbook")->execute();$session->sql("CREATE DATABASE addressbook")->execute();$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();$session->sql("INSERT INTO addressbook.names values ('John', 42), ('Sam', 33)")->execute();$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names") ;$row = $table->select('name', 'age')->execute()->fetchAll();print_r($row); `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => John
[age] => 42
)
[1] => Array
(
[name] => Sam
[age] => 33
)
)
