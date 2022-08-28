Встановлює критерії сортування

-   [« TableUpdate::limit](mysql-xdevapi-tableupdate.limit.html)
    
-   [TableUpdate::set »](mysql-xdevapi-tableupdate.set.html)
    
-   [PHP Manual](index.html)
    
-   [mysql\_xdevapi\\TableUpdate](class.mysql-xdevapi-tableupdate.html)
    
-   Встановлює критерії сортування
    

# TableUpdate::orderby

(No version information available, might only be in Git)

TableUpdate::orderby — Встановлює критерії сортування

### Опис

```methodsynopsis
public mysql_xdevapi\TableUpdate::orderby(mixed $orderby_expr, mixed ...$orderby_exprs): mysql_xdevapi\TableUpdate
```

Встановлює критерії сортування.

### Список параметрів

`orderby_expr`

Вирази, що визначають порядок за критеріями. Може бути масивом з одним або декількома виразами чи рядком.

`orderby_exprs`

Додаткові параметри sortexpr.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysqlxdevapiTableUpdate::orderby()****

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