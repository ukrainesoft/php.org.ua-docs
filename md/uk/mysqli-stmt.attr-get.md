---
navigation:
  - mysqli-stmt.affected-rows.md: '« mysqli\_stmt::$affected\_rows'
  - mysqli-stmt.attr-set.md: 'mysqli\_stmt::attr\_set »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::attr\_get'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::attr\_get

# mysqli\_stmt\_attr\_get

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::attr\_get -- mysqli\_stmt\_attr\_get — Отримує поточне значення атрибуту запиту

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::attr_get(int $attribute): int
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_attr_get(mysqli_stmt $statement, int $attribute): int
```

Використовується для отримання поточного атрибуту запиту.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`attribute`

Атрибут, який потрібно отримати.

### Значення, що повертаються

Повертає поточне значення атрибуту.
