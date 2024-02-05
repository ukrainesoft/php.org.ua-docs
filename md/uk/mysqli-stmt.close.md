---
navigation:
  - mysqli-stmt.bind-result.md: '« mysqli\_stmt::bind\_result'
  - mysqli-stmt.construct.md: 'mysqli\_stmt::\_\_construct »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::close'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::close

# mysqli\_stmt\_close

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::close -- mysqli\_stmt\_close — Закриває підготовлений запит

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::close(): true
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_close(mysqli_stmt $statement): true
```

Закриває підготовлений запит . **mysqli\_stmt\_close()** також звільняє дескриптор запиту. Якщо за поточним запитом отримано результат, ця функція очищає його для того, щоб міг бути виконаний наступний запит.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція тепер повертає значення **`true`**. . Раніше вона повертала значення \*\*`false`\*\*в случае возникновения ошибки. |

### Дивіться також

-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
