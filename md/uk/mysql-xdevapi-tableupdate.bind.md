- [«mysql_xdevapi\TableUpdate](class.mysql-xdevapi-tableupdate.md)
- [TableUpdate::\_\_construct »](mysql-xdevapi-tableupdate.construct.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableUpdate](class.mysql-xdevapi-tableupdate.md)
- Прив'язує параметри запиту на оновлення

# TableUpdate::bind

(No version information available, might only be in Git)

TableUpdate::bind — Прив'язує параметри запиту на оновлення

### Опис

public **mysql_xdevapi\TableUpdate::bind**(array `$placeholder_values`):
[mysql_xdevapi\TableUpdate](class.mysql-xdevapi-tableupdate.md)

Прив'язує значення до певного наповнювача.

### Список параметрів

`placeholder_values`
Ім'я заповнювача та значення для прив'язки, визначене як масив JSON.

### Значення, що повертаються

Об'єкт TableUpdate.

### Приклади

**Приклад #1 Приклад використання **mysql_xdevapi\TableUpdate::bind()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$table->update() ->set('status', 'admin')  ->where('name = :name and age > :age') ->bind(['name' => 'Bernie') , 'age' => 2000]) ->execute();?> `
