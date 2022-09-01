---
navigation:
  - mysql-xdevapi-rowresult.getwarningscount.html: '« RowResult::getWarningsCount'
  - mysql-xdevapi-schema.construct.html: 'Schema::construct »'
  - index.html: PHP Manual
  - book.mysql-xdevapi.html: Mysqlxdevapi
title: Клас Schema
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

-   [Schema::construct](mysql-xdevapi-schema.construct.html) - Конструктор
-   [Schema::createCollection](mysql-xdevapi-schema.createcollection.html) — Додати колекцію до схеми
-   [Schema::dropCollection](mysql-xdevapi-schema.dropcollection.html) — Видалити колекції зі схеми
-   [Schema::existsInDatabase](mysql-xdevapi-schema.existsindatabase.html) — Перевірити, чи існує у базі даних
-   [Schema::getCollection](mysql-xdevapi-schema.getcollection.html) — Отримати колекцію зі схеми
-   [Schema::getCollectionAsTable](mysql-xdevapi-schema.getcollectionastable.html) — Отримати об'єкт таблиці колекції
-   [Schema::getCollections](mysql-xdevapi-schema.getcollections.html) — Отримати всі колекції схеми
-   [Schema::getName](mysql-xdevapi-schema.getname.html) - Отримати ім'я схеми
-   [Schema::getSession](mysql-xdevapi-schema.getsession.html) — Здобути сесію схеми
-   [Schema::getTable](mysql-xdevapi-schema.gettable.html) — Отримати таблицю схеми
-   [Schema::getTables](mysql-xdevapi-schema.gettables.html) - Отримати таблиці схеми
