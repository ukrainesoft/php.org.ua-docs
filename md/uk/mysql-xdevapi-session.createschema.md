Створює нову схему

-   [« Session::construct](mysql-xdevapi-session.construct.html)
    
-   [Session::dropSchema »](mysql-xdevapi-session.dropschema.html)
    
-   [PHP Manual](index.md)
    
-   [mysqlxdevapiSession](class.mysql-xdevapi-session.html)
    
-   Створює нову схему
    

# Session::createSchema

(No version information available, might only be in Git)

Session::createSchema — Створює нову схему

### Опис

```methodsynopsis
public mysql_xdevapi\Session::createSchema(string $schema_name): mysql_xdevapi\Schema
```

Створює нову схему.

### Список параметрів

`schema_name`

Назва схеми для створення.

### Значення, що повертаються

Об'єкт Schema у разі успішного виконання у разі виникнення помилки видає виняток.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiSession::createSchema()****

```php
<?php
$uri  = 'mysqlx://happyuser:password@127.0.0.1:33060/';
$sess = mysql_xdevapi\getSession($uri);

try {

    if ($schema = $sess->createSchema('fruit')) {
        echo "Инфо: Я создал схему с именем 'fruit'\n";
    }

} catch (Exception $e) {

   echo $e->getMessage();

}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Инфо: Я создал схему с именем 'fruit'
```