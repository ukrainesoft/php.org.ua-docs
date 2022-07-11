- [« Result::getAutoIncrementValue](mysql-xdevapi-result.getautoincrementvalue.md)
- [Result::getWarnings »](mysql-xdevapi-result.getwarnings.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Result](class.mysql-xdevapi-result.md)
- Отримує згенеровані ідентифікатори

# Result::getGeneratedIds

(No version information available, might only be in Git)

Result::getGeneratedIds — Отримує згенеровані ідентифікатори

### Опис

public **mysql_xdevapi\Result::getGeneratedIds**(): array

Отримує згенеровані значення \_id із останньої операції. Унікальне
поле \_id генерується сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив згенерованих \_id з останньої операції або порожній масив,
якщо таких немає.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Result::getGeneratedIds()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$collection = $schema->get people");$result==$collection->add( '{"name": "Bernie",   "jobs": [{"title":"Cat Herder","Salary":42000}, {"title": "Father","Salary":0}],   "hobbies": ["Sports","Making cupcakes"]}', '{"name": "Jane",    "jobs": [{"title":" Scientist","Salary":18000}, {"title":"Mother","Salary":0}],   "hobbies": ["Walking","Making pies"]}')->execute(); $ids==$result->getGeneratedIds();var_dump($ids);?> `

Результатом виконання цього прикладу буде щось подібне:

array(2) {
[0]=>
string(28) "00005b6b5361000000000000064"
[1]=>
string(28) "00005b6b5361000000000000065"
}
