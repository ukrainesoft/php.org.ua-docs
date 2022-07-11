- [« Collection::addOrReplaceOne](mysql-xdevapi-collection.addorreplaceone.md)
- [Collection::count »](mysql-xdevapi-collection.count.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Collection](class.mysql-xdevapi-collection.md)
- Конструктор класу Collection

# Collection::\_\_construct

(No version information available, might only be in Git)

Collection::\_\_construct - Конструктор класу Collection

### Опис

private **mysql_xdevapi\Collection::\_\_construct**()

Створює об'єкт Collection.

### Список параметрів

Ця функція не має параметрів.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Collection::getOne()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema     = $session->getSchema("addressbook");$collection = $schema->createCollection("people");$result = $ {"name": "Alfred", "age": 42, "job": "Butler"}')->execute();// Унікальний _id (за замовчуванням і рекомендується) генерується MySQL Server// в цьому прикладі додано тільки одна запис, тому $ids[0]$ids        ==$result->getGeneratedIds();$alfreds_id = $ids[0];/$| >getOne($alfreds_id));?> `

Результатом виконання цього прикладу буде щось подібне:

00005b6b536100000000000001

Array
(
[_id] => 00005b6b53610000000000000b1
[age] => 42
[job] => Butler
[name] => Alfred
)
