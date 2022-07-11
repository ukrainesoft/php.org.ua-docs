- [«TableUpdate::limit](mysql-xdevapi-tableupdate.limit.md)
- [TableUpdate::set »](mysql-xdevapi-tableupdate.set.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableUpdate](class.mysql-xdevapi-tableupdate.md)
- Встановлює критерії сортування

# TableUpdate::orderby

(No version information available, might only be in Git)

TableUpdate::orderby — Встановлює критерії сортування

### Опис

public
**mysql_xdevapi\TableUpdate::orderby**([mixed](language.types.declarations.md#language.types.declarations.mixed)
`$orderby_expr`,
[mixed](language.types.declarations.md#language.types.declarations.mixed)
`...$orderby_exprs`):
[mysql_xdevapi\TableUpdate](class.mysql-xdevapi-tableupdate.md)

Встановлює критерії сортування.

### Список параметрів

`orderby_expr`
Вирази, що визначають порядок за критеріями. Може бути масивом
з одним або декількома виразами чи рядком.

`orderby_exprs`
Додаткові опції sort_expr.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableUpdate::orderby()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$res = $table->update()  ->set('level', 3) ->where('age > 15 and age < 22') ->limit(4) --orderby(['age asc ','name desc'])  ->execute();?> `
