---
navigation:
  - mysql-xdevapi-collection.count.md: '« Collection::count'
  - mysql-xdevapi-collection.dropindex.md: 'Collection::dropIndex »'
  - index.md: PHP Manual
  - class.mysql-xdevapi-collection.md: mysqlxdevapiCollection
title: 'Collection::createIndex'
---
# Collection::createIndex

(No version information available, might only be in Git)

Collection::createIndex — Створює індекс для колекції

### Опис

```methodsynopsis
public mysql_xdevapi\Collection::createIndex(string $index_name, string $index_desc_json): void
```

Створює індекс для колекції.

Видається виняток, якщо індекс із таким ім'ям вже існує, або якщо визначення індексу сформовано неправильно.

### Список параметрів

`index_name`

Ім'я індексу, який потрібно створити. Має бути коректним ім'ям індексу, допустимим для SQL-запиту `CREATE INDEX`

`index_desc_json`

Визначення індексу для створення. Містить масив об'єктів IndexField, і кожен об'єкт описує один елемент документа для додавання індексу, а також необов'язковий рядок для типу індексу, який може бути INDEX (за замовчуванням) або SPATIAL.

Один опис IndexField складається з наступних полів:

-   `field`: рядок, повний шлях документа до елемента документа чи поля для індексації
    
-   `type`: рядок, один із підтримуваних типів стовпців SQL для зіставлення поля. Для числових типів можна додати необов'язкове ключове слово UNSIGNED. Для типу TEXT може бути додана довжина для індексації.
    
-   `required`: булеве, (необов'язкове) true, якщо поле має бути обов'язковим у документі. За замовчуванням використовується значення **`false`**, за винятком типу `GEOJSON`, де за замовчуванням використовується значення **`true`**
    
-   `options`: ціле число, (необов'язкове) прапори спеціальних опцій для використання при декодуванні даних `GEOJSON`
    
-   `srid`: ціле число (необов'язкове) значення srid для використання при декодуванні даних `GEOJSON`
    

Помилково включати інші поля, не описані вище, до документів IndexDefinition або IndexField.

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiCollection::createIndex()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$session->sql("DROP DATABASE IF EXISTS addressbook")->execute();
$session->sql("CREATE DATABASE addressbook")->execute();

$schema     = $session->getSchema("addressbook");
$collection = $schema->createCollection("people");

// Создание текстового индекса
$collection->createIndex(
  'myindex1',
  '{"fields": [{
    "field": "$.name",
    "type": "TEXT(25)",
    "required": true}],
    "unique": false}'
);

// Пространственный индекс
$collection->createIndex(
  'myindex2',
  '{"fields": [{
    "field": "$.home",
    "type": "GEOJSON",
    "required": true}],
    "type": "SPATIAL"}'
);

// Индекс с несколькими полями
$collection->createIndex(
  'myindex3',
  '{"fields": [
    {
      "field": "$.name",
      "type": "TEXT(20)",
      "required": true
    },
    {
      "field": "$.age",
      "type": "INTEGER"
    },
    {
      "field": "$.job",
      "type": "TEXT(30)",
      "required": false
    }
  ],
  "unique": true
  }'
);
```
