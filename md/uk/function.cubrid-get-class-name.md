Отримує ім'я класу за допомогою OID

-   [« cubrid\_get\_charset](function.cubrid-get-charset.html)
    
-   [cubrid\_get\_client\_info »](function.cubrid-get-client-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримує ім'я класу за допомогою OID
    

# cubridgetclassname

(PECL CUBRID >= 8.3.0)

cubridgetclassname — Отримує ім'я класу за допомогою OID

### Опис

```methodsynopsis
cubrid_get_class_name(resource $conn_identifier, string $oid): string
```

Функція **cubridgetclassname()** використовується для отримання імені класу з параметра `oid`. Не працює при виборі даних із системних таблиць, наприклад dbclass.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення.

`oid`

OID екземпляра, існування якого необхідно перевірити.

### Значення, що повертаються

Ім'я класу при успішному завершенні процесу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridgetclassname()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code", CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);
$class_name = cubrid_get_class_name($conn, $oid);

print_r($class_name);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
code
```

### Дивіться також

-   [cubrid\_is\_instance()](function.cubrid-is-instance.html) - Перевіряє, чи існує екземпляр, на який вказує OID
-   [cubrid\_drop()](function.cubrid-drop.html) - Видалення екземпляра за OID