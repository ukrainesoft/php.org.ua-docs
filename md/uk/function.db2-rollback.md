---
navigation:
  - function.db2-result.md: « db2\_result
  - function.db2-server-info.md: db2\_server\_info »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_rollback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_rollback

(PECL ibm\_db2 >= 1.0.0)

db2\_rollback - Відкочує транзакцію

### Опис

```methodsynopsis
db2_rollback(resource $connection): bool
```

Відкочує поточну транзакцію на зазначеному з'єднанні та починає нову. За промовчанням, в PHP, використовується автопідтвердження транзакцій, так що функція **db2\_rollback()** потрібна лише в тому випадку, якщо ви примусово відключили автопідтвердження транзакцій для з'єднання.

### Список параметрів

`connection`

Змінна, що містить активний ресурс підключення, отриманий за допомогою [db2\_connect()](function.db2-connect.md) або [db2\_pconnect()](function.db2-pconnect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Відкат операції DELETE**

У наступному прикладі ми порахуємо кількість рядків у таблиці, відключимо автопідтвердження транзакцій, видалимо всі рядки у таблиці та переконаємось, що їх стало . Після цього ми використовуємо функцію **db2\_rollback()** і перевіримо, що число рядків у таблиці стало таким самим, як і до видалення - це підтвердить, що транзакція успішно відкотилася.

```php
<?php
$conn = db2_connect($database, $user, $password);

if ($conn) {
    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";

    // Отключаем автоподтверждение
    db2_autocommit($conn, DB2_AUTOCOMMIT_OFF);

    // Удаляем все строки из ANIMALS
    db2_exec($conn, "DELETE FROM animals");

    $stmt = db2_exec($conn, "SELECT count(*) FROM animals");
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";

    // Откатываем операцию DELETE
    db2_rollback( $conn );

    $stmt = db2_exec( $conn, "SELECT count(*) FROM animals" );
    $res = db2_fetch_array( $stmt );
    echo $res[0] . "\n";
    db2_close($conn);
}
?>
```

Результат виконання наведеного прикладу:

```
7
0
7
```

### Дивіться також

-   [db2\_autocommit()](function.db2-autocommit.md) \- Повертає або встановлює режим автопідтвердження транзакцій для з'єднання
-   [db2\_commit()](function.db2-commit.md) \- підтверджує транзакцію
