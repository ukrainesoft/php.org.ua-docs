---
navigation:
  - function.fdf-enum-values.md: « fdf\_enum\_values
  - function.fdf-error.md: fdf\_error »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdf\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fdf\_errno

(PHP 4 >= 4.3.0, PHP 5 < 5.3.0, PECL fdf SVN)

fdf\_errno — Повертає код помилки для останньої операції FDF

### Опис

```methodsynopsis
fdf_errno(): int
```

Отримує код помилки, встановлений останнім викликом функції FDF.

Текстовий опис помилки можна отримати за допомогою [fdf\_error()](function.fdf-error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повернення коду помилки як ціле число або нуль, якщо помилок не було.

### Дивіться також

-   [fdf\_error()](function.fdf-error.md) \- Повертає опис помилки для коду помилки FDF
