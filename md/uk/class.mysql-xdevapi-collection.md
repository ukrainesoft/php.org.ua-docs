---
navigation:
  - mysql-xdevapi-client.getsession.html: '« Client::getClient'
  - mysql-xdevapi-collection.add.html: 'Collection::add »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас Collection
---
# Клас Collection

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Collection
     

     implements 
       mysql_xdevapi\SchemaObject {

    /* Свойства */
    
     public
      $name;



    /* Методы */
    
   public add(mixed $document): mysql_xdevapi\CollectionAdd
public addOrReplaceOne(string $id, string $doc): mysql_xdevapi\Result
public count(): int
public createIndex(string $index_name, string $index_desc_json): void
public dropIndex(string $index_name): bool
public existsInDatabase(): bool
public find(string $search_condition = ?): mysql_xdevapi\CollectionFind
public getName(): string
public getOne(string $id): Document
public getSchema(): Schema Object
public getSession(): Session
public modify(string $search_condition): mysql_xdevapi\CollectionModify
public remove(string $search_condition): mysql_xdevapi\CollectionRemove
public removeOne(string $id): mysql_xdevapi\Result
public replaceOne(string $id, string $doc): mysql_xdevapi\Result

   }
```

## Властивості

name

## Зміст

-   [Collection::add](mysql-xdevapi-collection.add.html) — Додає документ у колекцію
-   [Collection::addOrReplaceOne](mysql-xdevapi-collection.addorreplaceone.html) — Додає або замінює документ колекції
-   [Collection::construct](mysql-xdevapi-collection.construct.html) - Конструктор класу Collection
-   [Collection::count](mysql-xdevapi-collection.count.html) — Отримує кількість документів
-   [Collection::createIndex](mysql-xdevapi-collection.createindex.html) — Створює індекс для колекції
-   [Collection::dropIndex](mysql-xdevapi-collection.dropindex.html) — Видаляє індекс колекції
-   [Collection::existsInDatabase](mysql-xdevapi-collection.existsindatabase.html) — Перевіряє, чи існує колекція у базі даних
-   [Collection::find](mysql-xdevapi-collection.find.html) - Шукає документ
-   [Collection::getName](mysql-xdevapi-collection.getname.html) — Отримує назву колекції
-   [Collection::getOne](mysql-xdevapi-collection.getone.html) — Отримує один документ
-   [Collection::getSchema](mysql-xdevapi-collection.getschema.html) — Повертає об'єкт Schema
-   [Collection::getSession](mysql-xdevapi-collection.getsession.html) — Повертає об'єкт Session
-   [Collection::modify](mysql-xdevapi-collection.modify.html) — Змінює документи колекції
-   [Collection::remove](mysql-xdevapi-collection.remove.html) — Видаляє документи колекції
-   [Collection::removeOne](mysql-xdevapi-collection.removeone.html) — Видаляє один документ із колекції
-   [Collection::replaceOne](mysql-xdevapi-collection.replaceone.html) — Замінює один документ колекції
