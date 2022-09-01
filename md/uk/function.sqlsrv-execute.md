---
navigation:
  - function.sqlsrv-errors.html: « sqlsrverrors
  - function.sqlsrv-fetch-array.html: sqlsrvfetcharray »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrvexecute
---
# sqlsrvexecute

(No version information available, might only be in Git)

sqlsrvexecute — Виконує запит, підготовлений за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.html)

### Опис

```methodsynopsis
sqlsrv_execute(resource $stmt): bool
```

Виконує запит, підготовлений за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.html). Функція ідеально підходить для багаторазового виконання підготовленого запиту з різними параметрами.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrvprepare()](function.sqlsrv-prepare.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvexecute()****

У цьому прикладі показано, як підготувати оператор за допомогою [sqlsrvprepare()](function.sqlsrv-prepare.html) та повторно виконати його кілька разів (з різними значеннями параметрів) за допомогою **sqlsrvexecute()**

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1
        SET OrderQty = ?
        WHERE SalesOrderID = ?";

// Инициализация параметров и подготовка запроса.
// Переменные $qty и $id связаны с оператором $stmt.
$qty = 0; $id = 0;
$stmt = sqlsrv_prepare( $conn, $sql, array( &$qty, &$id));
if( !$stmt ) {
    die( print_r( sqlsrv_errors(), true));
}

// Настройка информации SalesOrderDetailID и OrderQty.
// Этот Масив сопоставляет идентификатор заказа с количеством заказа в парах ключ => значение.
$orders = array( 1=>10, 2=>20, 3=>30);

// Выполнение запроса для каждого заказа.
foreach( $orders as $id => $qty) {
    // Поскольку $id и $qty привязаны к $stmt1,
    // их обновлённые значения используются при каждом выполнении запроса.
    if( sqlsrv_execute( $stmt ) === false ) {
          die( print_r( sqlsrv_errors(), true));
    }
}
?>
```

### Примітки

Коли ви підготуєте запит, який використовує змінні як параметри, змінні прив'язуються до оператора. Це означає, що якщо ви оновите значення змінних, наступного разу, коли ви виконаєте запит, він буде працювати з оновленими значеннями параметрів. Для операторів, які ви плануєте виконати лише один раз, використовуйте [sqlsrvquery()](function.sqlsrv-query.html)

### Дивіться також

-   [sqlsrvprepare()](function.sqlsrv-prepare.html) - готує запит до виконання
-   [sqlsrvquery()](function.sqlsrv-query.html) - готує та виконує запит
