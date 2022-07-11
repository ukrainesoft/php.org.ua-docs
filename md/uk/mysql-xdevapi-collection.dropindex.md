- [« Collection::createIndex](mysql-xdevapi-collection.createindex.md)
- [Collection::existsInDatabase »](mysql-xdevapi-collection.existsindatabase.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\Collection](class.mysql-xdevapi-collection.md)
- Видаляє індекс колекції

# Collection::dropIndex

(No version information available, might only be in Git)

Collection::dropIndex — Видаляє індекс колекції

### Опис

public **mysql_xdevapi\Collection::dropIndex**(string `$index_name`):
bool

Видаляє індекс колекції.

Ця операція не призведе до помилки, якщо індекс не
існує, але в цьому випадку повернеться **`false`**.

### Список параметрів

`index_name`
Ім'я індексу колекції видалення.

### Значення, що повертаються

**`true`**, якщо операція DROP INDEX виконана успішно, **`false`** в
інакше.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\Collection::dropIndex()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();$session->sql( "CREATE DATABASE addressbook")->execute();$schema==$session->getSchema("addressbook");$create = $schema->createCollection("people");// ...$collection = $s ->getCollection("people");$collection->createIndex( 'myindex', '{"fields": [{"field": "$.name", "type": "TEXT(25)", "required ": true}], "unique": false}');// ...if ($collection->dropIndex('myindex')) {    echo "Індекс з назвою 'myindex' був найден і лён ?> `

Результат виконання цього прикладу:

Індекс з назвою 'myindex' був знайдений та вилучений.
