- [«TableDelete::orderby](mysql-xdevapi-tabledelete.orderby.md)
- [mysql_xdevapi\TableInsert »](class.mysql-xdevapi-tableinsert.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableDelete](class.mysql-xdevapi-tabledelete.md)
- Встановлює умову пошуку для видалення

# TableDelete::where

(No version information available, might only be in Git)

TableDelete::where — Встановлює умову пошуку для видалення

### Опис

public **mysql_xdevapi\TableDelete::where**(string `$where_expr`):
[mysql_xdevapi\TableDelete](class.mysql-xdevapi-tabledelete.md)

Встановлює умову пошуку фільтрації.

### Список параметрів

`where_expr`
Визначає умову пошуку фільтрації документів або записів.

### Значення, що повертаються

Об'єкт TableDelete.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableDelete::where()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$table->delete() ->where("id = :id")  ->bind(['id' => 42])  ->limit(1) ->execute();?> `
