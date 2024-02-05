---
navigation:
  - function.sqlsrv-fetch.md: « sqlsrv\_fetch
  - function.sqlsrv-free-stmt.md: sqlsrv\_free\_stmt »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_field\_metadata
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_field\_metadata

(No version information available, might only be in Git)

sqlsrv\_field\_metadata — Отримує метадані для полів оператора, підготовленого за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md) або [sqlsrv\_query()](function.sqlsrv-query.md)

### Опис

```methodsynopsis
sqlsrv_field_metadata(resource $stmt): mixed
```

Отримує метадані для полів оператора, підготовленого за допомогою [sqlsrv\_prepare()](function.sqlsrv-prepare.md) або [sqlsrv\_query()](function.sqlsrv-query.md). . **sqlsrv\_field\_metadata()** може викликатися оператора до або після виконання оператора.

### Список параметрів

`stmt`

Ресурс оператора, для якого повертаються метадані.

### Значення, що повертаються

У разі успішного виконання повертає масив масивів. В іншому випадку повертає **`false`**. Кожен масив, що повертається, описується наступною таблицею:

**Масив, що повертається sqlsrv\_field\_metadata**

| Ключ | Опис |
| --- | --- |
| Name | Ім'я поля. |
| Type | Числове значення типу SQL. |
| Size | Кількість символів для полів символьного типу, кількість байтів для полів двійкового типу або **`null`** для інших типів. |
| Precision | Точність для типів змінної точності, **`null`** для інших типів. |
| Scale | Масштаб для типів масштабованих типів даних, **`null`** для інших типів. |
| Nullable | Перелік, що вказує, чи стовпець допускає значення NULL, неприпустиме значення NULL або невідоме. |

Для получения дополнительной информации смотрите[» sqlsrv\_field\_metadata](http://msdn.microsoft.com/en-us/library/cc296197.aspx)в документации Microsoft SQLSRV.

### Приклади

**Пример #1 Пример использования**sqlsrv\_field\_metadata()\*\*\*\*

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"AdventureWorks", "UID"=>"username", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);
if( $conn === false ) {
   die( print_r( sqlsrv_errors(), true));
}

$sql = "SELECT * FROM Table_1";
$stmt = sqlsrv_prepare( $conn, $sql );

foreach( sqlsrv_field_metadata( $stmt ) as $fieldMetadata ) {
    foreach( $fieldMetadata as $name => $value) {
       echo "$name: $value<br />";
    }
      echo "<br />";
}
?>
```

### Дивіться також

-   [sqlsrv\_client\_info()](function.sqlsrv-client-info.md) \- Повертає інформацію про клієнта та зазначене підключення
