- [«sqlsrv_errors](function.sqlsrv-errors.md)
- [sqlsrv_fetch_array »](function.sqlsrv-fetch-array.md)

- [PHP Manual](index.md)
- [Функції SQLSRV](ref.sqlsrv.md)
- Виконує запит підготовлений за допомогою sqlsrv_prepare

#sqlsrv_execute

(No version information available, might only be in Git)

sqlsrv_execute — Виконує запит, підготовлений за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md)

### Опис

**sqlsrv_execute**(resource `$stmt`): bool

Виконує запит, підготовлений за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md). Функція ідеальна
підходить для багаторазового виконання підготовленого запиту з різними
значення параметрів.

### Список параметрів

`stmt`
Ресурс оператора, що повертається
[sqlsrv_prepare()](function.sqlsrv-prepare.md).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **sqlsrv_execute()****

У цьому прикладі показано, як підготувати оператор за допомогою
[sqlsrv_prepare()](function.sqlsrv-prepare.md) та повторно виконати
його кілька разів (з різними значеннями параметрів) за допомогою
**sqlsrv_execute()**.

` <?php$serverName = "serverName\sqlexpress";$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");$conn = sqlsrv_connect ( $serverName, $connectionInfo);if( $conn === false) {    die( print_r( sqlsrv_errors(), true));}$sql = "UPDATE Table_1        SET OrderQty = ?        WHERE SalesOrderID = ?";// Инициализация параметрів і підготовка запиту.// Змінні $qty і $id пов'язані з оператором $stmt.$qty = 0; $id = 0;$stmt = sqlsrv_prepare( $conn, $sql, array( &$qty, &$id));if( !$stmt ) {    die( print_r( sqlsrv_error) Налаштування інформації SalesOrderDetailID і OrderQty.// Цей масив порівняє ідентифікатор замовлення з кількістю замовлення в парах ключ|=1=3               заказа.foreach( $orders as $id => $qty) {     // Оскільки $id і $qty прив'язані к $stmt1,    // их оновлені | if( sqlsrv_execute( $stmt ) ====false ) {         die( print_r( sqlsrv_errors(), true)); }}?> `

### Примітки

Коли ви підготуєте запит, який використовує змінні в
як параметри, змінні прив'язуються до оператора. Це означає,
що якщо ви оновите значення змінних, наступного разу, коли ви
виконайте запит, він буде працювати з оновленими значеннями
параметрів. Для операторів, які ви плануєте виконати лише один
раз, використовуйте [sqlsrv_query()](function.sqlsrv-query.md).

### Дивіться також

- [sqlsrv_prepare()](function.sqlsrv-prepare.md) - Підготовка
запит до виконання
- [sqlsrv_query()](function.sqlsrv-query.md) - Підготовляє та
виконує запит
