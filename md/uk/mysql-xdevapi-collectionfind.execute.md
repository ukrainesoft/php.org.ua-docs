- [« CollectionFind::\_\_construct](mysql-xdevapi-collectionfind.construct.md)
- [CollectionFind::fields »](mysql-xdevapi-collectionfind.fields.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\CollectionFind](class.mysql-xdevapi-collectionfind.md)
- Виконує затвердження

# CollectionFind::execute

(No version information available, might only be in Git)

CollectionFind::execute — Виконує затвердження

### Опис

public **mysql_xdevapi\CollectionFind::execute**():
[mysql_xdevapi\DocResult](class.mysql-xdevapi-docresult.md)

Виконує операцію пошуку; ця функціональність дозволена для ланцюжка
методів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Об'єкт DocResult, з якого можна отримати результати або запитати
стан операції.

### Приклади

**Приклад #1 Приклад використання CollectionFind**

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$create  ->add('{"name ": "Alfred", "age": 18, "job": "Butler"}') ->execute();// ...$collection =$$schema->getCollection("people");$result = $collection  ->find('job like :job and age > :age') ->bind(['job' => 'Butler', 'age' => 16]) ->execute();var_dump ->fetchAll());?> `

Результатом виконання цього прикладу буде щось подібне:

array(1) {
[0]=>
array(4) {
["_id"]=>
string(28) "00005b6b53610000000000000cf"
["age"]=>
int(18)
["job"]=>
string(6) "Butler"
["name"]=>
string(6) "Alfred"
}
}
