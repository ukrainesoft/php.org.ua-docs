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

-   [Schema::construct](mysql-xdevapi-schema.construct.md) - Конструктор
-   [Schema::createCollection](mysql-xdevapi-schema.createcollection.md) — Додати колекцію до схеми
-   [Schema::dropCollection](mysql-xdevapi-schema.dropcollection.md) — Видалити колекції зі схеми
-   [Schema::existsInDatabase](mysql-xdevapi-schema.existsindatabase.md) — Перевірити, чи існує у базі даних
-   [Schema::getCollection](mysql-xdevapi-schema.getcollection.md) — Отримати колекцію зі схеми
-   [Schema::getCollectionAsTable](mysql-xdevapi-schema.getcollectionastable.md) — Отримати об'єкт таблиці колекції
-   [Schema::getCollections](mysql-xdevapi-schema.getcollections.md) — Отримати всі колекції схеми
-   [Schema::getName](mysql-xdevapi-schema.getname.md) - Отримати ім'я схеми
-   [Schema::getSession](mysql-xdevapi-schema.getsession.md) — Здобути сесію схеми
-   [Schema::getTable](mysql-xdevapi-schema.gettable.md) — Отримати таблицю схеми
-   [Schema::getTables](mysql-xdevapi-schema.gettables.md) - Отримати таблиці схеми
