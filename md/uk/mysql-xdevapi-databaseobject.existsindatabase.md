Перевіряє, чи існує об'єкт у базі даних

-   [« mysqlxdevapiDatabaseObject](class.mysql-xdevapi-databaseobject.html)
    
-   [DatabaseObject::getName »](mysql-xdevapi-databaseobject.getname.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiDatabaseObject](class.mysql-xdevapi-databaseobject.html)
    
-   Перевіряє, чи існує об'єкт у базі даних
    

# DatabaseObject::existsInDatabase

(No version information available, might only be in Git)

DatabaseObject::existsInDatabase — Перевіряє, чи існує об'єкт у базі даних

### Опис

```methodsynopsis
abstract public mysql_xdevapi\DatabaseObject::existsInDatabase(): bool
```

Перевіряє, чи об'єкт бази даних посилається на об'єкт, який існує в базі даних.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо об'єкт існує в базі даних, інакше **`false`**, якщо це не так.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiDatabaseObject::existsInDatabase()****

```php
<?php

$existInDb = $dbObj->existsInDatabase();

?>
```