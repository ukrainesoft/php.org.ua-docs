---
navigation:
  - mysql-xdevapi-rowresult.getwarningscount.md: '« RowResult::getWarningsCount'
  - mysql-xdevapi-schema.construct.md: 'Schema::\_\_construct »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Клас Schema
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Schema

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\Schema
     

     implements 
       mysql_xdevapi\DatabaseObject {

    /* Свойства */
    
     public
      $name;



    /* Методы */
    
   public createCollection(string $name, string $validate = ?): mysql_xdevapi\Collection
public dropCollection(string $collection_name): bool
public existsInDatabase(): bool
public getCollection(string $name): mysql_xdevapi\Collection
public getCollectionAsTable(string $name): mysql_xdevapi\Table
public getCollections(): array
public getName(): string
public getSession(): mysql_xdevapi\Session
public getTable(string $name): mysql_xdevapi\Table
public getTables(): array

   }
```

## Властивості

name

## Зміст

-   [Schema::\_\_construct](mysql-xdevapi-schema.construct.md) \- Конструктор класу Schema
-   [Schema::createCollection](mysql-xdevapi-schema.createcollection.md)— Додає колекцію до схеми
-   [Schema::dropCollection](mysql-xdevapi-schema.dropcollection.md)— Видаляє колекції зі схеми
-   [Schema::existsInDatabase](mysql-xdevapi-schema.existsindatabase.md)— Перевіряє, чи існує у базі даних
-   [Schema::getCollection](mysql-xdevapi-schema.getcollection.md)— Отримує колекцію зі схеми
-   [Schema::getCollectionAsTable](mysql-xdevapi-schema.getcollectionastable.md)— Отримує колекцію як об'єкт класу Table
-   [Schema::getCollections](mysql-xdevapi-schema.getcollections.md)— Отримує всі колекції схеми
-   [Schema::getName](mysql-xdevapi-schema.getname.md)— Отримує ім'я схеми
-   [Schema::getSession](mysql-xdevapi-schema.getsession.md)— Отримує сесію схеми
-   [Schema::getTable](mysql-xdevapi-schema.gettable.md)— Отримує таблицю схеми
-   [Schema::getTables](mysql-xdevapi-schema.gettables.md)— Отримує таблиці схеми
