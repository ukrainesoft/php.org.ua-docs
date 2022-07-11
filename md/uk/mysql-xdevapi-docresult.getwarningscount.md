- [« DocResult::getWarnings](mysql-xdevapi-docresult.getwarnings.md)
- [mysql_xdevapi\Exception »](class.mysql-xdevapi-exception.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\DocResult](class.mysql-xdevapi-docresult.md)
- Отримати кількість попереджень з останньої операції

# DocResult::getWarningsCount

(No version information available, might only be in Git)

DocResult::getWarningsCount — Отримати кількість попереджень з
останньої операції

### Опис

public **mysql_xdevapi\DocResult::getWarningsCount**(): int

Повертає кількість попереджень, спричинених останньою операцією. В
зокрема ці попередження викликаються сервером MySQL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Кількість попереджень із останньої операції.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\DocResult::getWarningsCount()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema = $session->getSchema("addressbook");$create = $schema->createCollection("people");$create->add('{"name ": "Alfred", "age": 18, "job": "Butler"}')->execute();$create->add('{"name": "Reginald", "age": 42, "job": "Butler"}')->execute();// ...$collection = $schema->getCollection("people");// Повертає об'єкт DocResult$result = $collection ->find(' job like :job and age > :age') ->bind(['job' => 'Butler', 'age' => 16]) ->sort('age desc') ->execute(); !$result->getWarningsCount()) {    echo "Відбулася помилка:
";   print_r($result->getWarnings());   exit;}var_dump($result->fetchOne());?> `

Результатом виконання цього прикладу буде щось подібне:

array(4) {
["_id"]=>
string(28) "00005b6b5361000000000000135"
["age"]=>
int(42)
["job"]=>
string(6) "Butler"
["name"]=>
string(8) "Reginald"
}
