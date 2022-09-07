---
navigation:
  - function.cubrid-data-seek.md: « cubriddataseek
  - function.cubrid-errno.md: cubriderrno »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridдбname
---
# cubridдбname

(PECL CUBRID >= 8.3.1)

cubridдбname — Отримання імені бази даних із результату cubridlistdbs

### Опис

```methodsynopsis
cubrid_db_name(array $result, int $index): string
```

Витягує ім'я бази даних із результату виклику [cubridlistdbs()](function.cubrid-list-dbs.md)

### Список параметрів

`result`

Вказівник на результат виклику [cubridlistdbs()](function.cubrid-list-dbs.md)

`index`

Індекс в набір.

### Значення, що повертаються

Повертає ім'я бази даних у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо повернулося **`false`**, використовуйте [cubriderror()](function.cubrid-error.md) для точного визначення помилки, що відбулася.

### Приклади

**Приклад #1 Приклад використання **cubridдбname()****

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

Результат виконання цього прикладу:

```
demodb
```

### Дивіться також

-   [cubridlistdbs()](function.cubrid-list-dbs.md) - Отримати масив зі списком усіх баз даних CUBRID
