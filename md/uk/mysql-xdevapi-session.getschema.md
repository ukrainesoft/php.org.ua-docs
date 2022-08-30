Отримує новий об'єкт схеми

-   [« Session::getDefaultSchema](mysql-xdevapi-session.getdefaultschema.html)
    
-   [Session::getSchemas »](mysql-xdevapi-session.getschemas.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Отримує новий об'єкт схеми
    

# Session::getSchema

(No version information available, might only be in Git)

Session::getSchema — Отримує новий об'єкт схеми

### Опис

```methodsynopsis
public mysql_xdevapi\Session::getSchema(string $schema_name): mysql_xdevapi\Schema
```

Новий об'єкт Schema для вказаного імені схеми.

### Список параметрів

`schema_name`

Ім'я схеми (бази даних), на яку потрібно отримати об'єкт Schema.

### Значення, що повертаються

Об'єкт Schema.

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