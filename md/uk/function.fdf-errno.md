---
navigation:
  - function.fdf-enum-values.html: « fdfenumvalues
  - function.fdf-error.html: fdferror »
  - index.md: PHP Manual
  - ref.fdf.md: FDF
title: fdferrno
---
# fdferrno

(PHP 4> = 4.3.0, PHP 5 <5.3.0, PECL fdf SVN)

fdferrno — Повертає код помилки для останньої операції FDF

### Опис

```methodsynopsis
fdf_errno(): int
```

Отримує код помилки, встановлений останнім викликом функції FDF.

Текстовий опис помилки можна отримати за допомогою [fdferror()](function.fdf-error.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повернення коду помилки як ціле число або нуль, якщо помилок не було.

### Дивіться також

-   [fdferror()](function.fdf-error.md) - Повертає опис помилки для коду помилки FDF
