Робить наступний рядок у наборі результатів доступного для читання

-   [« sqlsrv\_fetch\_object](function.sqlsrv-fetch-object.html)
    
-   [sqlsrv\_field\_metadata »](function.sqlsrv-field-metadata.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Робить наступний рядок у наборі результатів доступного для читання
    

# sqlsrvfetch

(No version information available, might only be in Git)

sqlsrvfetch — Робить наступний рядок у наборі результатів, доступних для читання.

### Опис

```methodsynopsis
sqlsrv_fetch(resource $stmt, int $row = ?, int $offset = ?): mixed
```

Робить наступний рядок у наборі результатів, доступних для читання. Використовуйте [sqlsrv\_get\_field()](function.sqlsrv-get-field.html) для читання полів рядка.

### Список параметрів

`stmt`

Ресурс оператора, що повертається [sqlsrv\_query()](function.sqlsrv-query.html) або [sqlsrv\_execute()](function.sqlsrv-execute.html)

`row`

Рядок, до якого потрібно отримати доступ. Параметр можна використовувати лише в тому випадку, якщо вказаний оператор був підготовлений за допомогою курсору з можливістю прокручування. У цьому випадку параметр може приймати одне з таких значень:

-   SQLSRVSCROLLNEXT
-   SQLSRVSCROLLPRIOR
-   SQLSRVSCROLLFIRST
-   SQLSRVSCROLLLAST
-   SQLSRVSCROLLABSOLUTE
-   SQLSRVSCROLLRELATIVE

`offset`

Вказує рядок, до якого буде доступ, якщо для параметра рядка встановлено значення **`SQLSRV_SCROLL_ABSOLUTE`** або **`SQLSRV_SCROLL_RELATIVE`**. Зауважте, що перший рядок у наборі результатів має індекс 0.

### Значення, що повертаються

Повертає **`true`**, якщо наступний рядок набору результатів було успішно отримано, **`false`** у разі виникнення помилки та **`null`**якщо у наборі результатів більше немає рядків.

### Приклади

**Приклад #1 Приклад використання **sqlsrvfetch()****

У наступному прикладі показано, як отримати рядок за допомогою **sqlsrvfetch()** та отримати поля рядки за допомогою [sqlsrv\_get\_field()](function.sqlsrv-get-field.html)

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
     die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT Name, Comment
        FROM Table_1
        WHERE ReviewID=1";
$stmt = sqlsrv_query( $conn, $sql);
if( $stmt === false ) {
     die( print_r( sqlsrv_errors(), true));
}

// Сделайте первую (и в данном случае единственную) строку набора результатов доступной для чтения.
if( sqlsrv_fetch( $stmt ) === false) {
     die( print_r( sqlsrv_errors(), true));
}

// Получите поля строки. Индексы полей начинаются с 0 и должны извлекаться по порядку.
// Получение полей строки по имени не поддерживается sqlsrv_get_field.
$name = sqlsrv_get_field( $stmt, 0);
echo "$name: ";

$comment = sqlsrv_get_field( $stmt, 1);
echo $comment;
?>
```

### Дивіться також

-   [sqlsrv\_get\_field()](function.sqlsrv-get-field.html) - Отримує дані поля з поточного вибраного рядка
-   [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.html) - Повертає рядок як масив
-   [sqlsrv\_fetch\_object()](function.sqlsrv-fetch-object.html) - Отримує наступний рядок даних у наборі результатів як об'єкт