---
navigation:
  - function.get-html-translation-table.md: « get\_html\_translation\_table
  - function.hebrevc.md: hebrevc »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: hebrev
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hebrev

(PHP 4, PHP 5, PHP 7, PHP 8)

hebrev — Перетворює текст на івриті з логічного кодування на візуальне

### Опис

```methodsynopsis
hebrev(string $string, int $max_chars_per_line = 0): string
```

Перетворює текст на івриті з логічного кодування на візуальне.

Ця функція намагається уникнути розривів слів.

### Список параметрів

`string`

Вхідний рядок на івриті.

`max_chars_per_line`

Цей необов'язковий параметр вказує число символів, що максимально повертається, на рядок.

### Значення, що повертаються

Повертає рядок у візуальному кодуванні.

### Дивіться також

-   [hebrevc()](function.hebrevc.md) \- Перетворює текст на івриті з логічного кодування на візуальне з перетворенням перекладу рядка
