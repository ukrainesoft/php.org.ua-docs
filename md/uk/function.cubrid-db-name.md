---
navigation:
  - function.cubrid-data-seek.md: « cubrid\_data\_seek
  - function.cubrid-errno.md: cubrid\_errno »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_db\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_db\_name

(PECL CUBRID >= 8.3.1)

cubrid\_db\_name — Отримання імені бази даних із результату cubrid\_list\_dbs

### Опис

```methodsynopsis
cubrid_db_name(array $result, int $index): string
```

Витягує ім'я бази даних із результату виклику [cubrid\_list\_dbs()](function.cubrid-list-dbs.md)

### Список параметрів

`result`

Вказівник на результат виклику [cubrid\_list\_dbs()](function.cubrid-list-dbs.md)

`index`

Індекс в набір.

### Значення, що повертаються

Повертає ім'я бази даних у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо повернулося **`false`**, используйте[cubrid\_error()](function.cubrid-error.md) для точного визначення помилки, що відбулася.

### Приклади

**Пример #1 Пример использования**cubrid\_db\_name()\*\*\*\*

```php
<?php
error_reporting(E_ALL);

$conn = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$db_list = cubrid_list_dbs($conn);

$i = 0;
$cnt = count($db_list);
while ($i < $cnt) {
    echo cubrid_db_name($db_list, $i) . "\n";
    $i++;
}
?>
```

Результат виконання наведеного прикладу:

```
demodb
```

### Дивіться також

-   [cubrid\_list\_dbs()](function.cubrid-list-dbs.md) \- Отримати масив зі списком усіх баз даних CUBRID
