- [« TableSelect::lockExclusive](mysql-xdevapi-tableselect.lockexclusive.md)
- [TableSelect::offset »](mysql-xdevapi-tableselect.offset.md)

- [PHP Manual](index.md)
- [mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)
- Виконує SHARED LOCK

# TableSelect::lockShared

(No version information available, might only be in Git)

TableSelect::lockShared — Виконує SHARED LOCK

### Опис

public **mysql_xdevapi\TableSelect::lockShared**(int
`$lock_waiting_option` = ?):
[mysql_xdevapi\TableSelect](class.mysql-xdevapi-tableselect.md)

Виконує операцію читання із SHARED LOCK. Тільки один замок може бути
активним одночасно.

### Список параметрів

`lock_waiting_option`
Необов'язковий параметр очікування, який за замовчуванням дорівнює
**`MYSQLX_LOCK_DEFAULT`**. Допустимі значення:

- **`MYSQLX_LOCK_DEFAULT`**

- **`MYSQLX_LOCK_NOWAIT`**

- **`MYSQLX_LOCK_SKIP_LOCKED`**

### Значення, що повертаються

Об'єкт TableSelect.

### Приклади

**Приклад #1 Приклад використання
**mysql_xdevapi\TableSelect::lockShared()****

` <?php$session = mysql_xdevapi\getSession("mysqlx://user:password@localhost");$schema = $session->getSchema("addressbook");$table  = $schema->getTable("names" );$session->startTransaction();$result = $table->select('name', 'age') ->lockShared(MYSQLX_LOCK_NOWAIT) ->execute();$session->commit();$row == $result->fetchAll();print_r($row);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[name] => John
[age] => 42
)
[1] => Array
(
[name] => Sam
[age] => 42
)
)
