- [« Result::\_\_construct](mysql-xdevapi-result.construct.md)
- [Result::getAutoIncrementValue »](mysql-xdevapi-result.getautoincrementvalue.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Result](class.mysql-xdevapi-result.md)
- Отримує кількість порушених рядків

# Result::getAffectedItemsCount

(No version information available, might only be in Git)

Result::getAffectedItemsCount — Отримує кількість порушених рядків

### Опис

public **mysql_xdevapi\Result::getAffectedItemsCount**(): int

Отримує кількість рядків, порушених попередньою операцією.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість (як ціле число) порушених рядків.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Result::getAffectedItemsCount()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$collection = $schema->get people");$result = $collection->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();var_dump( $res- >getAffectedItemsCount() );?> `

Результат виконання цього прикладу:

int(1)
