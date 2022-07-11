- [« CollectionModify::arrayInsert](mysql-xdevapi-collectionmodify.arrayinsert.md)
- [CollectionModify::\_\_construct »](mysql-xdevapi-collectionmodify.construct.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)
- Прив'язує значення до заповнювача запиту

# CollectionModify::bind

(No version information available, might only be in Git)

CollectionModify::bind — Прив'язує значення до заповнювача запиту

### Опис

public **mysql_xdevapi\CollectionModify::bind**(array
`$placeholder_values`):
[mysql_xdevapi\CollectionModify](class.mysql-xdevapi-collectionmodify.md)

Прив'язує параметр до заповнювача за умови пошуку операції зміни.

Заповнювач має вигляд :NAME, де ':' - це загальний префікс, який має
завжди існувати до будь-якого NAME, де NAME це ім'я заповнювача.
Метод bind приймає список заповнювачів, якщо за умови пошуку операції
зміни необхідно замінити на кілька об'єктів.

### Список параметрів

`placeholder_values`
Підстановкові значення для заміни за умови пошуку. Допускається
використання кількох значень, які необхідно передати у вигляді
масиву зіставлень PLACEHOLDER_NAME-\>PLACEHOLDER_VALUE.

### Значення, що повертаються

Об'єкт CollectionModify, який можна використовувати для виконання
команди або додавання додаткових операцій.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\CollectionModify::bind()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema     = $session->getSchema("addressbook");$collection = $schema->createCollection("people");$result =  {"name":   "Bernie",    "traits": ["Friend", "Brother", "Human"]}') ->execute();$collection  ->modify("name = :name")  bind(['name' => 'Bernie']) ->arrayAppend('traits', 'Happy') ->execute();$result = $collection  ->find() --execute();print_r($ result->fetchAll());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[_id] => 00005b6b5361000000000000110
[name] => Bernie
[traits] => Array
(
[0] => Friend
[1] => Brother
[2] => Human
[3] => Happy
)
)
)
