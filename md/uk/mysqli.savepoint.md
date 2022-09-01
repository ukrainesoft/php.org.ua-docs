---
navigation:
  - mysqli.rollback.html: '« mysqli::rollback'
  - mysqli.select-db.html: 'mysqli::selectdb »'
  - index.html: PHP Manual
  - class.mysqli.html: mysqli
title: 'mysqli::savepoint'
---
# mysqli::savepoint

# mysqlisavepoint

(PHP 5> = 5.5.0, PHP 7, PHP 8)

mysqli::savepoint -- mysqlisavepoint — Встановіть іменовану точку збереження транзакції.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::savepoint(string $name): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_savepoint(mysqli $mysql, string $name): bool
```

Функція ідентична до виконання запиту ``$mysqli->query("SAVEPOINT `$name`");``

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.html)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqlireleasesavepoint()](mysqli.release-savepoint.html) - Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
