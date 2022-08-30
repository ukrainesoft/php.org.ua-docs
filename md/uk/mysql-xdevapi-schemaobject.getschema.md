Отримує об'єкт схеми

-   [« mysqlxdevapiSchemaObject](class.mysql-xdevapi-schemaobject.html)
    
-   [mysqlxdevapiSession »](class.mysql-xdevapi-session.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSchemaObject](class.mysql-xdevapi-schemaobject.html)
    
-   Отримує об'єкт схеми
    

# SchemaObject::getSchema

(No version information available, might only be in Git)

SchemaObject::getSchema — Отримує об'єкт схеми

### Опис

```methodsynopsis
abstract mysql_xdevapi\SchemaObject::getSchema(): mysql_xdevapi\Schema
```

Використовується іншими об'єктами для отримання схеми об'єкта.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний об'єкт Schema.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::getSchema()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");
$schema  = $session->getSchema("addressbook");

print_r($schema);
```

Результатом виконання цього прикладу буде щось подібне:

```
mysql_xdevapi\Schema Object
(
    [name] => addressbook
)
```