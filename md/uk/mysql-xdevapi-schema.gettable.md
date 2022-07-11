- [« Schema::getSession](mysql-xdevapi-schema.getsession.md)
- [Schema::getTables »](mysql-xdevapi-schema.gettables.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Schema](class.mysql-xdevapi-schema.md)
- Отримати таблицю схеми

# Schema::getTable

(No version information available, might only be in Git)

Schema::getTable — Отримати таблицю схеми

### Опис

public **mysql_xdevapi\Schema::getTable**(string `$name`):
[mysql_xdevapi\Table](class.mysql-xdevapi-table.md)

Отримання об'єкта Table для зазначеної таблиці у схемі.

### Список параметрів

`name`
Ім'я таблиці.

### Значення, що повертаються

Об'єкт Table.

### Приклади

**Приклад #1 Приклад використання **mysql_xdevapi\Schema::getTable()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$session->sql("CREATE TABLE addressbook.names(name text, age int)")->execute();$session->sql("INSERT INTO addressbook. names values ('John', 42), ('Sam', 33)")->execute();$schema = $session->getSchema("addressbook");$table  ==$schema->getTable("names ");$row = $table->select('name', 'age')->execute()->fetchAll();print_r($row);?> `

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
