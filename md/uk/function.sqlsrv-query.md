---
navigation:
  - function.sqlsrv-prepare.md: « sqlsrv\_prepare
  - function.sqlsrv-rollback.md: sqlsrv\_rollback »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_query

(No version information available, might only be in Git)

sqlsrv\_query — Підготовка та виконання запиту

### Опис

```methodsynopsis
sqlsrv_query(    resource $conn,    string $sql,    array $params = ?,    array $options = ?): mixed
```

Підготовляє та виконує запит.

### Список параметрів

`conn`

Ресурс підключення, що повертається [sqlsrv\_connect()](function.sqlsrv-connect.md)

`sql`

Рядок, що визначає запит, який потрібно підготувати та виконати.

`params`

Масив, що визначає інформацію про параметри під час параметризованого запиту. Елементи масиву можуть бути будь-якими з наступних:

-   Строкового значення
-   Змінної PHP
-   Масиву з наступною структурою: array($value\[, $direction\[, $phpType\[, $sqlType\]\]\]) .

У наступній таблиці описані елементи у структурі масиву вище:

**Структура масиву**

| Элемент | Опис |
| --- | --- |
| $value | Рядкове значення, змінна PHP або змінна PHP, передана за посиланням. |
| $direction (optional) | Одна з наступних констант SQLSRV, що використовуються для вказівки напряму параметра: SQLSRV\_PARAM\_IN, SQLSRV\_PARAM\_OUT, SQLSRV\_PARAM\_INOUT. Значення за промовчанням - SQLSRV\_PARAM\_IN. |
| $phpType (optional) | Константа SQLSRV\_PHPTYPE\_\*, що вказує тип даних PHP значення, що повертається. |
| $sqlType (optional) | Константа SQLSRV\_SQLTYPE\_\*вказує тип даних SQL Server вхідного значення. |

`options`

Масив, визначальний параметри властивостей запиту. Ключі, що підтримуються, описані в наступній таблиці:

**Властивості запиту**

| Ключ | Значения | Опис |
| --- | --- | --- |
| QueryTimeout | Позитивне ціле значення. | Встановлює час очікування в секундах. За замовчуванням драйвер чекатиме на результати нескінченно. |
| SendStreamParamsAtExec | **`true`** або **`false`** (за замовчуванням **`true`**) . | Налаштовує драйвер для надсилання всіх даних потоку під час виконання (**`true`**) або для надсилання даних потоку частинами (**`false`**). За замовчуванням встановлено значення **`true`**. . Для отримання додаткової інформації дивіться [sqlsrv\_send\_stream\_data()](function.sqlsrv-send-stream-data.md) |
| Scrollable | SQLSRV\_CURSOR\_FORWARD, SQLSRV\_CURSOR\_STATIC, SQLSRV\_CURSOR\_DYNAMIC, або SQLSRV\_CURSOR\_KEYSET | Смотрите[» Вказівка ​​типу курсору та вибір рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)в документации Microsoft SQLSRV. |

### Значення, що повертаються

Повертає ресурс виразу у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** sqlsrv\_query()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "INSERT INTO Table_1 (id, data) VALUES (?, ?)";
$params = array(1, "some data");

$stmt = sqlsrv_query( $conn, $sql, $params);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}
?>
```

### Примітки

Для операторів, які ви плануєте виконати лише один раз, використовуйте **sqlsrv\_query()**. Якщо ви маєте намір повторно виконати вираз з іншими параметрами, використовуйте комбінацію [sqlsrv\_prepare()](function.sqlsrv-prepare.md) і [sqlsrv\_execute()](function.sqlsrv-execute.md)

### Дивіться також

-   [sqlsrv\_prepare()](function.sqlsrv-prepare.md) \- готує запит до виконання
-   [sqlsrv\_execute()](function.sqlsrv-execute.md) \- Виконує запит підготовлений за допомогою sqlsrv\_prepare
