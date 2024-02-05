---
navigation:
  - function.sqlsrv-errors.md: « sqlsrv\_errors
  - function.sqlsrv-fetch-array.md: sqlsrv\_fetch\_array »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_execute

(No version information available, might only be in Git)

sqlsrv\_execute — Виконує запит, підготовлений за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md)

### Опис

```methodsynopsis
sqlsrv_execute(resource $stmt): bool
```

Виконує запит, підготовлений за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md). Функція ідеально підходить для багаторазового виконання підготовленого запиту з різними параметрами.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrv\_prepare()](function.sqlsrv-prepare.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**sqlsrv\_execute()\*\*\*\*

У цьому прикладі показано, як підготувати оператор за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md) та повторно виконати його кілька разів (з різними значеннями параметрів) за допомогою **sqlsrv\_execute()**

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false) {
    die( print_r( sqlsrv_errors(), true));
}

$sql = "UPDATE Table_1
        SET OrderQty = ?
        WHERE SalesOrderID = ?";

// Инициализация параметров и подготовка запроса.
// Переменные $qty и $id связаны с оператором $stmt.
$qty = 0; $id = 0;
$stmt = sqlsrv_prepare( $conn, $sql, array( &$qty, &$id));
if( !$stmt ) {
    die( print_r( sqlsrv_errors(), true));
}

// Настройка информации SalesOrderDetailID и OrderQty.
// Этот массив сопоставляет идентификатор заказа с количеством заказа в парах ключ => значение.
$orders = array( 1=>10, 2=>20, 3=>30);

// Выполнение запроса для каждого заказа.
foreach( $orders as $id => $qty) {
    // Поскольку $id и $qty привязаны к $stmt1,
    // их обновлённые значения используются при каждом выполнении запроса.
    if( sqlsrv_execute( $stmt ) === false ) {
          die( print_r( sqlsrv_errors(), true));
    }
}
?>
```

### Примітки

Коли ви підготуєте запит, який використовує змінні як параметри, змінні прив'язуються до оператора. Це означає, що якщо ви оновите значення змінних, наступного разу, коли ви виконаєте запит, він буде працювати з оновленими значеннями параметрів. Для операторів, які ви плануєте виконати лише один раз, використовуйте [sqlsrv\_query()](function.sqlsrv-query.md)

### Дивіться також

-   [sqlsrv\_prepare()](function.sqlsrv-prepare.md) \- готує запит до виконання
-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
