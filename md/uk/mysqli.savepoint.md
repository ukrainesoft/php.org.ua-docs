---
navigation:
  - mysqli.rollback.md: '« mysqli::rollback'
  - mysqli.select-db.md: 'mysqli::select\_db »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::savepoint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::savepoint

# mysqli\_savepoint

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

mysqli::savepoint -- mysqli\_savepoint — Встановіть іменовану точку збереження транзакції.

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mysqli\_release\_savepoint()](mysqli.release-savepoint.md) \- Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
