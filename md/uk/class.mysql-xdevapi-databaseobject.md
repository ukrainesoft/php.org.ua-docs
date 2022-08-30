Інтерфейс DatabaseObject

-   [« CrudOperationSortable::sort](mysql-xdevapi-crudoperationsortable.sort.html)
    
-   [DatabaseObject::existsInDatabase »](mysql-xdevapi-databaseobject.existsindatabase.html)
    
-   [PHP Manual](index.html)
    
-   [Mysqlxdevapi](book.mysql-xdevapi.html)
    
-   Інтерфейс DatabaseObject
    

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

-   [DatabaseObject::existsInDatabase](mysql-xdevapi-databaseobject.existsindatabase.html) — Перевіряє, чи існує об'єкт у базі даних
-   [DatabaseObject::getName](mysql-xdevapi-databaseobject.getname.html) — Отримує ім'я об'єкта
-   [DatabaseObject::getSession](mysql-xdevapi-databaseobject.getsession.html) — Отримує ім'я сесії