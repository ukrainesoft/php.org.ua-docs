- [« CollectionModify::patch](mysql-xdevapi-collectionmodify.patch.md)
- [CollectionModify::set »](mysql-xdevapi-collectionmodify.set.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)
- Замінює поле документа

# CollectionModify::replace

(No version information available, might only be in Git)

CollectionModify::replace — Замінює поле документа

### Опис

public **mysql_xdevapi\CollectionModify::replace**(string
`$collection_field`, string `$expression_or_literal`):
[mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)

Замінює (оновлює) це значення поля новим.

### Список параметрів

`collection_field`
Шлях документа до елемента оновлення.

`expression_or_literal`
Значення, яке встановлюється для зазначеного атрибута.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\CollectionModify::replace()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema     = $session->getSchema("addressbook");$collection = $schema->createCollection("people");$result =  {"name":   "Bernie",    "traits": ["Friend", "Brother", "Human"]}') ->execute();$collection  ->modify("name = :name")  bind(['name' => 'Bernie'])  ->replace("name", "Bern") ->execute();$result = $collection ->find() ->execute();print_r($ result->fetchAll());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[_id] => 00005b6b536100000000000011b
[name] => Bern
[traits] => Array
(
[0] => Friend
[1] => Brother
[2] => Human
)
)
)
