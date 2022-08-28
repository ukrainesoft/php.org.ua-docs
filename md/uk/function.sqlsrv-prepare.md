Підготовка запиту до виконання

-   [« sqlsrv\_num\_rows](function.sqlsrv-num-rows.html)
    
-   [sqlsrv\_query »](function.sqlsrv-query.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Підготовка запиту до виконання
    

# sqlsrvprepare

(No version information available, might only be in Git)

sqlsrvprepare — Підготовка запиту до виконання

### Опис

```methodsynopsis
sqlsrv_prepare(    resource $conn,    string $sql,    array $params = ?,    array $options = ?): mixed
```

Підготовка запиту до виконання. Функція ідеально підходить для підготовки запиту, який виконуватиметься кілька разів із різними значеннями параметрів.

### Список параметрів

`conn`

Ресурс підключення, що повертається [sqlsrv\_connect()](function.sqlsrv-connect.html)

`sql`

Рядок, що визначає запит, який потрібно підготувати та виконати.

`params`

Масив, що визначає інформацію про параметри під час виконання запиту. Елементи масиву можуть бути будь-якими з наступних:

-   Строкове значення
-   Змінна PHP
-   Масив із такою структурою: array($value , $Direction , $phpType , $sqlType

У наступній таблиці описані елементи у структурі масиву вище:

**Структура масиву**

| Элемент | Описание |
| --- | --- |
| $value | Рядкове значення, змінна PHP або змінна PHP, передана за посиланням. |
| $direction (необов'язковий) | Одна з наступних констант SQLSRV, що використовуються для вказівки напряму параметра: SQLSRVPARAMIN, SQLSRVPARAMOUT, SQLSRVPARAMINOUT. Значення за промовчанням - SQLSRVPARAMIN. |
| $phpType (необов'язковий) | Константа SQLSRVPHPTYPE, що вказує тип даних PHP значення, що повертається. |
| $sqlType (необов'язковий) | Константа SQLSRVSQLTYPEвказує тип даних SQL Server вхідного значення. |

`options`

Масив, що визначає параметри властивостей запиту. Ключі, що підтримуються, описані в наступній таблиці:

**Опції запиту**

| Ключ | Значения | Описание |
| --- | --- | --- |
| QueryTimeout | Позитивне ціле значення. | Встановлює час очікування в секундах. За замовчуванням драйвер очікуватиме результатів нескінченно. |
| SendStreamParamsAtExec | **`true`** або **`false`** (за замовчуванням **`true`** | Налаштовує драйвер для надсилання всіх даних потоку під час виконання (**`true`**) або для надсилання даних потоку частинами (**`false`**). За замовчуванням встановлено значення **`true`**. Для отримання додаткової інформації дивіться [sqlsrv\_send\_stream\_data()](function.sqlsrv-send-stream-data.html) |
| Scrollable | SQLSRVCURSORFORWARD, SQLSRVCURSORSTATIC, SQLSRVCURSORDYNAMIC, або SQLSRVCURSORKEYSET | Дивіться [» Указание типа курсора и выбор строк](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV. |

### Значення, що повертаються

Повертає ресурс оператора у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrvprepare()****

У цьому прикладі показано, як підготувати оператор за допомогою **sqlsrvprepare()** та повторно виконати його кілька разів (з різними значеннями параметрів) за допомогою [sqlsrv\_execute()](function.sqlsrv-execute.html)

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
// Этот массив сопоставляет идентификатор заказа с количеством заказа в парах ключ => значение.
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

Коли ви підготуєте запит, який використовує змінні як параметри, змінні прив'язуються до оператора. Це означає, що якщо ви оновите значення змінних, наступного разу, коли ви виконаєте запит, він буде працювати з оновленими значеннями параметрів. Для операторів, які ви плануєте виконати лише один раз, використовуйте [sqlsrv\_query()](function.sqlsrv-query.html)

### Дивіться також

-   [sqlsrv\_execute()](function.sqlsrv-execute.html) - Виконує запит підготовлений за допомогою sqlsrvprepare
-   [sqlsrv\_query()](function.sqlsrv-query.html) - готує та виконує запит