- [« CollectionModify::replace](mysql-xdevapi-collectionmodify.replace.md)
- [CollectionModify::skip »](mysql-xdevapi-collectionmodify.skip.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)
- Встановлює атрибут документа

# CollectionModify::set

(No version information available, might only be in Git)

CollectionModify::set — Встановлює атрибут документа

### Опис

public **mysql_xdevapi\CollectionModify::set**(string
`$collection_field`, string `$expression_or_literal`):
[mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)

Встановлює або оновлює атрибути документів у колекції.

### Список параметрів

`collection_field`
Шлях до документа (ім'я) елемента для встановлення.

`expression_or_literal`
Значення установки.

### Значення, що повертаються

Об'єкт CollectionModify.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\CollectionModify::set()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema     = $session->getSchema("addressbook");$collection = $schema->createCollection("people");$result =  {"name":   "Bernie",    "traits": ["Friend", "Brother", "Human"]}') ->execute();$collection  ->modify("name = :name")  bind(['name' => 'Bernie'])  ->set("name", "Bern") ->execute();$result = $collection ->find() ->execute();print_r($ result->fetchAll());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[_id] => 00005b6b5361000000000000111
[name] => Bern
[traits] => Array
(
[0] => Friend
[1] => Brother
[2] => Human
)
)
)
