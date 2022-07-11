- [« Collection::getName](mysql-xdevapi-collection.getname.md)
- [Collection::getSchema »](mysql-xdevapi-collection.getschema.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Collection](class.mysql-xdevapi-collection.md)
- Отримує один документ

# Collection::getOne

(No version information available, might only be in Git)

Collection::getOne — Отримує один документ

### Опис

public **mysql_xdevapi\Collection::getOne**(string `$id`): Document

Вибирає один документ із колекції.

Це короткий запис для:
`Collection.find("_id = :id").bind("id", id).execute().fetchOne();`

### Список параметрів

`id`
\_id документи в колекції.

### Значення, що повертаються

Об'єкт колекції або **null, якщо \_id не відповідає документу.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Collection::getOne()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema     = $session->getSchema("addressbook");$collection = $schema->createCollection("people");$result = $ {"name": "Alfred", "age": 42, "job": "Butler"}')->execute();// Унікальний _id (за замовчуванням і рекомендується) генерується MySQL Server// в цьому прикладі тільки один запис, тому $ids[0]$ids        = $result->getGeneratedIds();$alfreds_id ==$$s[0];// ...print_$ getOne($alfreds_id));?> `

Результатом виконання цього прикладу буде щось подібне:

00005b6b536100000000000001

Array
(
[_id] => 00005b6b53610000000000000b1
[age] => 42
[job] => Butler
[name] => Alfred
)
