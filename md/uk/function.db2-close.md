---
navigation:
  - function.db2-client-info.md: « db2\_client\_info
  - function.db2-column-privileges.md: db2\_column\_privileges »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_close

(PECL ibm\_db2 >= 1.0.0)

db2\_close — Закриває з'єднання з базою даних

### Опис

```methodsynopsis
db2_close(resource $connection): bool
```

Функція закриває з'єднання з базою DB2, створене за допомогою [db2\_connect()](function.db2-connect.md) та повертає відповідні ресурси серверу баз даних.

Якщо ви спробуєте закрити постійне з'єднання, створене за допомогою [db2\_pconnect()](function.db2-pconnect.md), запит на закриття буде проігнорований і з'єднання буде доступне для подальшого використання.

### Список параметрів

`connection`

Активне з'єднання з DB2.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Закриття з'єднання**

Наступний приклад демонструє успішну спробу закрити з'єднання з IBM DB2, Cloudscape або базою даних Apache Derby.

```php
<?php
$conn = db2_connect('SAMPLE', 'db2inst1', 'ibmdb2');
$rc = db2_close($conn);
if ($rc) {
    echo "Соединение закрыто.";
}
?>
```

Результат виконання наведеного прикладу:

```
Соединение закрыто.
```

### Дивіться також

-   [db2\_connect()](function.db2-connect.md) \- Повертає з'єднання з базою даних
-   [db2\_pclose()](function.db2-pclose.md) \- Закриває постійне з'єднання з базою даних
-   [db2\_pconnect()](function.db2-pconnect.md) \- Повертає постійне з'єднання з базою даних
