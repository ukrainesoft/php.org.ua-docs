---
navigation:
  - mysql-xdevapi-client.getsession.md: '« Client::getClient'
  - mysql-xdevapi-collection.add.md: 'Collection::add »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас Collection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

-   [Collection::add](mysql-xdevapi-collection.add.md)— Додає документ у колекцію
-   [Collection::addOrReplaceOne](mysql-xdevapi-collection.addorreplaceone.md)— Додає або замінює документ колекції
-   [Collection::\_\_construct](mysql-xdevapi-collection.construct.md) \- Конструктор класу Collection
-   [Collection::count](mysql-xdevapi-collection.count.md)— Отримує кількість документів
-   [Collection::createIndex](mysql-xdevapi-collection.createindex.md)— Створює індекс для колекції
-   [Collection::dropIndex](mysql-xdevapi-collection.dropindex.md)— Видаляє індекс колекції
-   [Collection::existsInDatabase](mysql-xdevapi-collection.existsindatabase.md)— Перевіряє, чи існує колекція у базі даних
-   [Collection::find](mysql-xdevapi-collection.find.md) \- Шукає документ
-   [Collection::getName](mysql-xdevapi-collection.getname.md)— Отримує назву колекції
-   [Collection::getOne](mysql-xdevapi-collection.getone.md)— Отримує один документ
-   [Collection::getSchema](mysql-xdevapi-collection.getschema.md)— Повертає об'єкт Schema
-   [Collection::getSession](mysql-xdevapi-collection.getsession.md)— Повертає об'єкт Session
-   [Collection::modify](mysql-xdevapi-collection.modify.md)— Змінює документи колекції
-   [Collection::remove](mysql-xdevapi-collection.remove.md)— Видаляє документи колекції
-   [Collection::removeOne](mysql-xdevapi-collection.removeone.md)— Видаляє один документ із колекції
-   [Collection::replaceOne](mysql-xdevapi-collection.replaceone.md)— Замінює один документ колекції
