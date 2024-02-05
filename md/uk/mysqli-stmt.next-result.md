---
navigation:
  - mysqli-stmt.more-results.md: '« mysqli\_stmt::more\_results'
  - mysqli-stmt.num-rows.md: 'mysqli\_stmt::$num\_rows »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::next\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::next\_result

# mysqli\_stmt\_next\_result

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

mysqli\_stmt::next\_result -- mysqli\_stmt\_next\_result — Читає наступний набір рядків із мультизапиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::next_result(): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_stmt_next_result(mysqli_stmt $statement): bool
```

Читає наступний набір рядків із мультизапиту.

> **Зауваження** :
> 
> До PHP 8.1.0, функція доступна лише з [mysqlnd](book.mysqlnd.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Тепер також доступно при збиранні з libmysqlclient. |

### Дивіться також

-   [mysqli\_stmt::more\_results()](mysqli-stmt.more-results.md) \- Перевіряє, чи є ще набори рядків внаслідок мультизапиту
-   [mysqli::multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
