---
navigation:
  - pdo.getattribute.md: '« PDO::getAttribute'
  - pdo.intransaction.md: 'PDO::inTransaction »'
  - index.md: PHP Manual
  - class.pdo.md: PDO
title: 'PDO::getAvailableDrivers'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDO::getAvailableDrivers

# pdo\_drivers

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 1.0.3)

PDO::getAvailableDrivers -- pdo\_drivers — Повертає масив доступних драйверів PDO

### Опис

```methodsynopsis
public static PDO::getAvailableDrivers(): array
```

```methodsynopsis
pdo_drivers(): array
```

Ця функція повертає всі наявні в даний час драйвери PDO, які можна використовувати в `DSN`\-параметре[PDO::\_\_construct()](pdo.construct.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функция**PDO::getAvailableDrivers()** повертає масив імен PDO драйверів. Якщо немає драйверів, повертається порожній масив.

### Приклади

**Приклад #1 Приклад виконання **PDO::getAvailableDrivers()****

```php
<?php
print_r(PDO::getAvailableDrivers());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => mysql
    [1] => sqlite
)
```
