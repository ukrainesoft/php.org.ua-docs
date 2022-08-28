Повертає OID поточної позиції курсору

-   [« cubrid\_connect](function.cubrid-connect.html)
    
-   [cubrid\_disconnect »](function.cubrid-disconnect.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Повертає OID поточної позиції курсору
    

# cubridcurrentoid

(PECL CUBRID >= 8.3.0)

cubridcurrentoid — Повертає OID поточної позиції курсору

### Опис

```methodsynopsis
cubrid_current_oid(resource $req_identifier): string
```

Функція **cubridcurrentoid()** використовується для одержання oid поточного положення курсору в результуючому наборі. Для використання функції **cubridcurrentoid()**, запущений запит повинен бути оновлюваним, і при запуску запиту було встановлено опцію **`CUBRID_INCLUDE_OID`**

### Список параметрів

`req_identifier`

Ідентифікатор запиту.

### Значення, що повертаються

Oid поточного положення курсору, у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridcurrentoid()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$res = cubrid_get($conn, $oid);

print_r($res);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Array
(
    [s_name] => X
    [f_name] => Mixed
)
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.html) - Виконує підготовлений SQL-оператор