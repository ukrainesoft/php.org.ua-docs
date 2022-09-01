---
navigation:
  - mysqli.refresh.md: '« mysqli::refresh'
  - mysqli.rollback.md: 'mysqli::rollback »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::releasesavepoint'
---
# mysqli::releasesavepoint

# mysqlireleasesavepoint

(PHP 5> = 5.5.0, PHP 7, PHP 8)

mysqli::releasesavepoint - mysqlireleasesavepoint — Видалити іменовану точку збереження зі списку точок збереження поточної транзакції.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::release_savepoint(string $name): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_release_savepoint(mysqli $mysql, string $name): bool
```

Функція ідентична до виконання запиту ``$mysqli->query("RELEASE SAVEPOINT `$name`");``. Вона не запускає фіксацію чи відкат.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.html) або [mysqliinit()](mysqli.init.md)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqlisavepoint()](mysqli.savepoint.md) - Встановіть іменовану точку збереження транзакції
