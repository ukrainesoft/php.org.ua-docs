- [« mysql_xdevapi\CollectionFind](class.mysql-xdevapi-collectionfind.md)
- [CollectionFind::\_\_construct »](mysql-xdevapi-collectionfind.construct.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\CollectionFind](class.mysql-xdevapi-collectionfind.md)
- Прив'язує значення до заповнювача запиту

# CollectionFind::bind

(No version information available, might only be in Git)

CollectionFind::bind — Прив'язує значення до заповнювача запиту

### Опис

public **mysql_xdevapi\CollectionFind::bind**(array
`$placeholder_values`):
[mysql_xdevapi\CollectionFind](class.mysql-xdevapi-collectionfind.md)

Дозволяє користувачеві прив'язати параметр до заповнювача за умови пошуку
операції пошуку. Заповнювач має вигляд :NAME, де ':' - це загальний
префікс, який повинен завжди існувати перед будь-яким NAME, NAME -
фактичне ім'я наповнювача. Функція bind приймає список наповнювачів,
якщо за умов пошуку необхідно замінити кілька об'єктів.

### Список параметрів

`placeholder_values`
Значення для підстановки за умов пошуку; допускається кілька
значень, що передаються у вигляді масиву, де "PLACEHOLDER_NAME =\>
PLACEHOLDER_VALUE".

### Значення, що повертаються

Об'єкт CollectionFind, або ланцюжок з execute() для повернення об'єкту
Result.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\CollectionFind::bind()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$result = $create  ->ad {"name": "Alfred", "age": 18, "job": "Butler"}') ->execute();// ...$collection = $schema->getCollection("people"); $result = $collection ->find('job like :job and age > :age') ->bind(['job' => 'Butler', 'age' => 16])  ->execute ($result->fetchAll());?> `

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
