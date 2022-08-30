Перевіряє, чи існує екземпляр, на який вказує OID

-   [« cubridinsertід](function.cubrid-insert-id.html)
    
-   [cubridlobclose »](function.cubrid-lob-close.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Перевіряє, чи існує екземпляр, на який вказує OID
    

# cubridісinstance

(PECL CUBRID >= 8.3.0)

cubridісinstance — Перевіряє, чи існує екземпляр, на який вказує OID

### Опис

```methodsynopsis
cubrid_is_instance(resource $conn_identifier, string $oid): int
```

Функція **cubridісinstance()** використовується, щоб перевірити, чи існує екземпляр, на який вказує даний `oid`, чи ні.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення.

`oid`

OID екземпляра, існування якого потрібно перевірити.

### Значення, що повертаються

1, якщо такий екземпляр існує;

0, якщо такого екземпляра немає;

1 у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridісinstance()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$sql = <<<EOD
SELECT host_year, medal, game_date
FROM game
WHERE athlete_code IN
    (SELECT code FROM athlete WHERE name='Thorpe Ian');
EOD;

$req = cubrid_execute($conn, $sql, CUBRID_INCLUDE_OID);
$oid = cubrid_current_oid($req);

$res = cubrid_is_instance ($conn, $oid);
if ($res == 1) {
    echo "Экземпляр, на который указывает $oid, существует.\n";
} else if ($res == 0){
    echo "Экземпляр, на который указывает $oid, не существует.\n";
} else {
    echo "Ошибка\n";
}

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Экземпляр, на который указывает @0|0|0, не существует.
```

### Дивіться також

-   [cubriddrop()](function.cubrid-drop.html) - Видалення екземпляра за OID
-   [cubridgetclassname()](function.cubrid-get-class-name.html) - Отримує ім'я класу за допомогою OID