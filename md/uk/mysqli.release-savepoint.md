---
navigation:
  - mysqli.refresh.md: '« mysqli::refresh'
  - mysqli.rollback.md: 'mysqli::rollback »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::release\_savepoint'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::release\_savepoint

# mysqli\_release\_savepoint

(PHP 5 >= 5.5.0, PHP 7, PHP 8)

mysqli::release\_savepoint -- mysqli\_release\_savepoint — Видалити іменовану точку збереження зі списку точок збереження поточної транзакції.

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [mysqli\_savepoint()](mysqli.savepoint.md) \- Встановіть іменовану точку збереження транзакції
