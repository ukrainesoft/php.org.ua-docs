- [« DocResult::fetchOne](mysql-xdevapi-docresult.fetchone.md)
- [DocResult::getWarningsCount »](mysql-xdevapi-docresult.getwarningscount.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\DocResult](class.mysql-xdevapi-docresult.md)
- Отримати попередження з останньої операції

# DocResult::getWarnings

(No version information available, might only be in Git)

DocResult::getWarnings — Отримати попередження з останньої операції

### Опис

public **mysql_xdevapi\DocResult::getWarnings**(): Array

Отримує попередження від останньої операції з сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів із попередженнями, спричиненими останньою операцією.
Кожен об'єкт містить поля 'message', 'level' та 'code'. Повертає
порожній масив, якщо немає помилок.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\DocResult::getWarnings()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$create->add('{"name ": "Alfred", "age": 18, "job": "Butler"}')->execute();$create->add('{"name": "Reginald", "age": 42, "job": "Butler"}')->execute();// ...$collection = $schema->getCollection("people");// Повертає об'єкт DocResult$result = $collection ->find(' job like :job and age > :age') ->bind(['job' => 'Butler', 'age' => 16]) ->sort('age desc') ->execute(); !$result->getWarningsCount()) {    echo "Відбулася помилка:
";   print_r($result->getWarnings());   exit;}var_dump($result->fetchOne());?> `

Результатом виконання цього прикладу буде щось подібне:


There was an error:

Array
(
[0] => mysql_xdevapi\Warning Object
(
[message] => Something bad and so on
[level] => 2
[code] => 1365
)
[1] => mysql_xdevapi\Warning Object
(
[message] => Something bad and so on
[level] => 2
[code] => 1365
)
)
