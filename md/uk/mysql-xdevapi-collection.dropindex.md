---
navigation:
  - mysql-xdevapi-collection.createindex.md: '« Collection::createIndex'
  - mysql-xdevapi-collection.existsindatabase.md: 'Collection::existsInDatabase »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysql\_xdevapi\\Collection
title: 'Collection::dropIndex'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Collection::dropIndex

(No version information available, might only be in Git)

Collection::dropIndex — Видаляє індекс колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::dropIndex(string $index_name): bool
```

Видаляє індекс колекції.

Ця операція не призведе до помилки, якщо індекс не існує, але в цьому випадку повернеться **`false`**

### Список параметрів

`index_name`

Ім'я індексу колекції видалення.

### Значення, що повертаються

\*\*`true`\*\*якщо операція DROP INDEX виконана успішно, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання** mysql\_xdevapi\\Collection::dropIndex()\*\*\*\*

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema = $session->getSchema("addressbook");
$create = $schema->createCollection("people");

// ...

$collection = $schema->getCollection("people");

$collection->createIndex(
  'myindex',
  '{"fields": [{"field": "$.name", "type": "TEXT(25)", "required": true}], "unique": false}'
);

// ...

if ($collection->dropIndex('myindex')) {
    echo "Индекс с названием 'myindex' был найден и удалён.";
}
?>
```

Результат виконання наведеного прикладу:

```
Индекс с названием 'myindex' был найден и удалён.
```
