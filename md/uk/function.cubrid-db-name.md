Отримання імені бази даних з результату cubridlistdbs

-   [« cubrid\_data\_seek](function.cubrid-data-seek.html)
    
-   [cubrid\_errno »](function.cubrid-errno.html)
    
-   [PHP Manual](index.html)
    
-   [Функции совместимости CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Отримання імені бази даних з результату cubridlistdbs
    

# cubridдбname

(PECL CUBRID >= 8.3.1)

cubridдбname — Отримання імені бази даних із результату cubridlistdbs

### Опис

```methodsynopsis
cubrid_db_name(array $result, int $index): string
```

Витягує ім'я бази даних із результату виклику [cubrid\_list\_dbs()](function.cubrid-list-dbs.html)

### Список параметрів

`result`

Вказівник на результат виклику [cubrid\_list\_dbs()](function.cubrid-list-dbs.html)

`index`

Індекс в набір.

### Значення, що повертаються

Повертає ім'я бази даних у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо повернулося **`false`**, використовуйте [cubrid\_error()](function.cubrid-error.html) для точного визначення помилки, що відбулася.

### Приклади

**Приклад #1 Приклад використання **cubridдбname()****

```php
<?php
error_reporting(E_ALL);

$conn = cubrid_connect('localhost', 33000, 'demodb', 'dba', '');
$db_list = cubrid_list_dbs($conn);

$i = 0;
$cnt = count($db_list);
while ($i < $cnt) {
    echo cubrid_db_name($db_list, $i) . "\n";
    $i++;
}
?>
```

Результат виконання цього прикладу:

```
demodb
```

### Дивіться також

-   [cubrid\_list\_dbs()](function.cubrid-list-dbs.html) - Отримати масив зі списком усіх баз даних CUBRID