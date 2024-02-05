---
navigation:
  - mysqli-stmt.insert-id.md: '« mysqli\_stmt::$insert\_id'
  - mysqli-stmt.next-result.md: 'mysqli\_stmt::next\_result »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::more\_results'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::more\_results

# mysqli\_stmt\_more\_results

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli\_stmt::more\_results -- mysqli\_stmt\_more\_results — Перевіряє, чи є ще набори рядків через мультизапит.

### Опис

Об'єктно-орієнтований стиль:

```methodsynopsis
public mysqli_stmt::more_results(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_more_results(mysqli_stmt $statement): bool
```

Перевіряє, чи є ще набори рядків через мультизапит.

> **Зауваження** :
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`**, якщо є доступні результуючі набори, **`false`** в іншому випадку.

### Дивіться також

-   [mysqli\_stmt::next\_result()](mysqli-stmt.next-result.md) \- Читає наступний набір рядків із мультизапиту
-   [mysqli::multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
