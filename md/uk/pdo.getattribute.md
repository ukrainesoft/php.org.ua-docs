---
navigation:
  - pdo.exec.md: '« PDO::exec'
  - pdo.getavailabledrivers.md: 'PDO::getAvailableDrivers »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::getAttribute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::getAttribute

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.0)

PDO::getAttribute — Отримує атрибут з'єднання з базою даних

### Опис

```methodsynopsis
public PDO::getAttribute(int $attribute): mixed
```

Ця функція повертає значення атрибута з'єднання з базою даних. Щоб отримати атрибути об'єкта PDOStatement, звертаються до методу [PDOStatement::getAttribute()](pdostatement.getattribute.md)

Зверніть увагу, що не всі комбінації бази даних/драйвер підтримують всі атрибути з'єднання з базою даних.

### Список параметрів

`attribute`

Одна из констант`PDO::ATTR_*`. Список загальних атрибутів, що застосовуються до підключень до бази даних:

-   `PDO::ATTR_AUTOCOMMIT`
-   `PDO::ATTR_CASE`
-   `PDO::ATTR_CLIENT_VERSION`
-   `PDO::ATTR_CONNECTION_STATUS`
-   `PDO::ATTR_DRIVER_NAME`
-   `PDO::ATTR_ERRMODE`
-   `PDO::ATTR_ORACLE_NULLS`
-   `PDO::ATTR_PERSISTENT`
-   `PDO::ATTR_PREFETCH`
-   `PDO::ATTR_SERVER_INFO`
-   `PDO::ATTR_SERVER_VERSION`
-   `PDO::ATTR_TIMEOUT`

Деякі драйвери можуть використовувати додаткові, характерні для цього драйвера, атрибути. Зверніть увагу, що атрибути драйвера *не повинні* використовувати з іншими драйверами.

### Значення, що повертаються

Повертає значення атрибута запитаного PDO (при успішному виклику). Невдалий виклик повертає `null`

### Помилки

Метод**PDO::getAttribute()** може викинути виняток [PDOException](class.pdoexception.md), коли базовий драйвер не підтримує запитаний у параметрі `attribute`атрибут.

### Приклади

**Приклад #1 Отримання атрибутів з'єднання з базою даних**

```php
<?php
$conn = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');
$attributes = array(
    "AUTOCOMMIT", "ERRMODE", "CASE", "CLIENT_VERSION", "CONNECTION_STATUS",
    "ORACLE_NULLS", "PERSISTENT", "PREFETCH", "SERVER_INFO", "SERVER_VERSION",
    "TIMEOUT"
);

foreach ($attributes as $val) {
    echo "PDO::ATTR_$val: ";
    echo $conn->getAttribute(constant("PDO::ATTR_$val")) . "\n";
}
?>
```

### Дивіться також

-   [PDO::setAttribute()](pdo.setattribute.md) \- Встановлення атрибуту
-   [PDOStatement::getAttribute()](pdostatement.getattribute.md) \- Отримання значення атрибуту запиту PDOStatement
-   [PDOStatement::setAttribute()](pdostatement.setattribute.md) \- Встановлює атрибут об'єкту PDOStatement
