Додає поле для оновлення

-   [« TableUpdate::orderby](mysql-xdevapi-tableupdate.orderby.html)
    
-   [TableUpdate::where »](mysql-xdevapi-tableupdate.where.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlxdevapiTableUpdate](class.mysql-xdevapi-tableupdate.html)
    
-   Додає поле для оновлення
    

# TableUpdate::set

(No version information available, might only be in Git)

TableUpdate::set — Додає поле для оновлення

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::set(string $table_field, string $expression_or_literal): mysql_xdevapi\TableUpdate
```

Оновлює значення стовпця для записів у таблиці.

### Список параметрів

`table_field`

Ім'я стовпця, що підлягає оновленню.

`expression_or_literal`

Значення, яке буде встановлене у вказаному стовпці.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::set()****

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