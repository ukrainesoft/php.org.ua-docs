---
navigation:
  - mysqli.kill.md: '« mysqli::kill'
  - mysqli.multi-query.md: 'mysqli::multi\_query »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::more\_results'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::more\_results

# mysqli\_more\_results

(PHP 5, PHP 7, PHP 8)

mysqli::more\_results -- mysqli\_more\_results — Перевірка, чи є ще результати мультизапиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::more_results(): bool
```

Процедурний стиль

```methodsynopsis
mysqli_more_results(mysqli $mysql): bool
```

Вказує, чи є доступні результуючі набори від попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.md)

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертається **`true`** у випадку, якщо один або більше результуючих наборів (включно з помилками) доступні після попереднього виклику функції [mysqli\_multi\_query()](mysqli.multi-query.md), иначе\*\*`false`\*\*

### Приклади

Смотрите[mysqli\_multi\_query()](mysqli.multi-query.md)

### Дивіться також

-   [mysqli\_multi\_query()](mysqli.multi-query.md) \- Виконує один або кілька запитів до бази даних
-   [mysqli\_next\_result()](mysqli.next-result.md) \- Підготовка наступного доступного результуючого набору з multi\_query
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
