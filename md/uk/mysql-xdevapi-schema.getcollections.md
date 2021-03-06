- [« Schema::getCollectionAsTable](mysql-xdevapi-schema.getcollectionastable.md)
- [Schema::getName »](mysql-xdevapi-schema.getname.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Schema](class.mysql-xdevapi-schema.md)
- Отримати всі колекції схеми

# Schema::getCollections

(No version information available, might only be in Git)

Schema::getCollections — Отримати всі колекції схеми

### Опис

public **mysql_xdevapi\Schema::getCollections**(): array

Отримати список колекцій для цієї схеми.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив усіх колекцій у цій схемі, де кожне значення елемента масиву
є об'єктом Collection з ім'ям колекції як ключ.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Schema::getCollections()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$collect = $schema->createCollection("people");$collect->add('{"name ": "Fred",  "age": 21, "job": "Construction"}')->execute();$collect->add('{"name": "Wilma", "age": 23, "job": "Teacher"}')->execute();$collections = $schema->getCollections();var_dump($collections);?> `

Результатом виконання цього прикладу буде щось подібне:

array(1) {
["people"]=>
object(mysql_xdevapi\Collection)#4 (1) {
["name"]=>
string(6) "people"
}
}
