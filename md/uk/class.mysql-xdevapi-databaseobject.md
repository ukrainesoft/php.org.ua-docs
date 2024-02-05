---
navigation:
  - mysql-xdevapi-crudoperationsortable.sort.md: '« CrudOperationSortable::sort'
  - mysql-xdevapi-databaseobject.existsindatabase.md: 'DatabaseObject::existsInDatabase »'
  - index.md: PHP Manual
  - book.mysql-xdevapi.md: Mysql\_xdevapi
title: Інтерфейс DatabaseObject
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс DatabaseObject

(PECL mysql-xdevapi >= 8.0.11)

## Вступ

## Огляд класів

```classsynopsis



    
     
      class mysql_xdevapi\DatabaseObject
     
     {


    /* Методы */
    
   abstract public existsInDatabase(): bool
abstract public getName(): string
abstract public getSession(): mysql_xdevapi\Session

   }
```

## Зміст

-   [DatabaseObject::existsInDatabase](mysql-xdevapi-databaseobject.existsindatabase.md)— Перевіряє, чи існує об'єкт у базі даних
-   [DatabaseObject::getName](mysql-xdevapi-databaseobject.getname.md)— Отримує ім'я об'єкта
-   [DatabaseObject::getSession](mysql-xdevapi-databaseobject.getsession.md)— Отримує ім'я сесії
