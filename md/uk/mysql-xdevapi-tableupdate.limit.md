Обмежує кількість рядків для оновлення

-   [« TableUpdate::execute](mysql-xdevapi-tableupdate.execute.html)
    
-   [TableUpdate::orderby »](mysql-xdevapi-tableupdate.orderby.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\TableUpdate](class.mysql-xdevapi-tableupdate.html)
    
-   Обмежує кількість рядків для оновлення
    

# TableUpdate::limit

(No version information available, might only be in Git)

TableUpdate::limit — Обмежує кількість рядків для оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::limit(int $rows): mysql_xdevapi\TableUpdate
```

Встановлює максимальну кількість записів або документів поновлення.

### Список параметрів

`rows`

Максимальна кількість записів чи документів для оновлення.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::limit()****

```php
<?php
$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");

$schema = $session->getSchema("addressbook");
$table  = $schema->getTable("names");

$res = $table->update()
  ->set('level', 3)
  ->where('age > 15 and age < 22')
  ->limit(4)
  ->orderby(['age asc','name desc'])
  ->execute();

?>
```