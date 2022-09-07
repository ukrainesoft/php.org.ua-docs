---
navigation:
  - mysqli-stmt.affected-rows.md: '« mysqlistmt::$affectedrows'
  - mysqli-stmt.attr-set.md: 'mysqlistmt::attrset »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqlistmt
title: 'mysqlistmt::attrget'
---
# mysqlistmt::attrget

# mysqlistmtattrget

(PHP 5, PHP 7, PHP 8)

mysqlistmt::attrget - mysqlistmtattrget — Отримує поточне значення атрибуту запиту

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

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.md), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.md)

`attribute`

Атрибут, який потрібно отримати.

### Значення, що повертаються

Повертає поточне значення атрибуту.
