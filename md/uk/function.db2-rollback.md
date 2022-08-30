Відкочує транзакцію

-   [« db2result](function.db2-result.html)
    
-   [db2serverinfo »](function.db2-server-info.html)
    
-   [PHP Manual](index.html)
    
-   [Функції IBM DB2](ref.ibm-db2.html)
    
-   Відкочує транзакцію
    

# db2rollback

(PECL ibmdb2> = 1.0.0)

db2rollback - Відкочує транзакцію

### Опис

```methodsynopsis
db2_rollback(resource $connection): bool
```

Відкочує поточну транзакцію на зазначеному з'єднанні та починає нову. За промовчанням, в PHP, використовується автопідтвердження транзакцій, так що функція **db2rollback()** потрібна лише в тому випадку, якщо ви примусово відключили автопідтвердження транзакцій для з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2connect()](function.db2-connect.html) або [db2pconnect()](function.db2-pconnect.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Відкат операції DELETE**

У наступному прикладі ми порахуємо кількість рядків у таблиці, відключимо автопідтвердження транзакцій, видалимо всі рядки у таблиці та переконаємось, що їх стало `0`. Після цього ми використовуємо функцію **db2rollback()** і перевіримо, що число рядків у таблиці стало таким самим, як і до видалення - це підтвердить, що транзакція успішно відкотилася.

```php
<?php
$conn = db2_connect($database, $user, $password);

if ($conn) {
    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";

    // Отключаем автоподтверждение
    db2_autocommit($conn, DB2_AUTOCOMMIT_OFF);

    // Удаляем все строки из ANIMALS
    db2_exec($conn, "DELETE FROM animals");

    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";

    // Откатываем операцию DELETE
    db2_rollback( $conn );

    $stmt = db2_exec( $conn, "SELECT count(*) FROM animals" );
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";
    db2_close($conn);
}
?>
```

Результат виконання цього прикладу:

```
7
0
7
```

### Дивіться також

-   [db2autocommit()](function.db2-autocommit.html) - Повертає або встановлює режим автопідтвердження транзакцій для з'єднання
-   [db2commit()](function.db2-commit.html) - підтверджує транзакцію