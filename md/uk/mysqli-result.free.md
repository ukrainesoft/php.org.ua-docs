---
navigation:
  - mysqli-result.field-seek.md: '« mysqli\_result::field\_seek'
  - mysqli-result.getiterator.md: 'mysqli\_result::getIterator »'
  - index.md: PHP Manual
  - class.mysqli-result.md: mysqli\_result
title: 'mysqli\_result::free'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_result::free

# mysqli\_result::close

# mysqli\_result::free\_result

# mysqli\_free\_result

(PHP 5, PHP 7, PHP 8)

mysqli\_result::free -- mysqli\_result::close -- mysqli\_result::free\_result -- mysqli\_free\_result — Звільняє пам'ять, зайняту результатами запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_result::free(): void
```

```methodsynopsis
public mysqli_result::close(): void
```

```methodsynopsis
public mysqli_result::free_result(): void
```

Процедурний стиль

```methodsynopsis
mysqli_free_result(mysqli_result $result): void
```

Визволяє пам'ять, зайняту результатами запиту.

### Список параметрів

`result`

Тільки для процедурного стилю: об'єкт [mysqli\_result](class.mysqli-result.md), який повернула функція [mysqli\_query()](mysqli.query.md) [mysqli\_store\_result()](mysqli.store-result.md) [mysqli\_use\_result()](mysqli.use-result.md) або [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [mysqli\_query()](mysqli.query.md) \- Виконує запит до бази даних
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
-   [mysqli\_use\_result()](mysqli.use-result.md) \- Готує результуючий набір на сервері для використання
