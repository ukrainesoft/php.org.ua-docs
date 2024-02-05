---
navigation:
  - function.property-exists.md: « property\_exists
  - book.ctype.md: Ctype »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: trait\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# trait\_exists

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

trait\_exists — Перевіряє, чи існує трейт

### Опис

```methodsynopsis
trait_exists(string $trait, bool $autoload = true): bool
```

### Список параметрів

`trait`

Ім'я трейту для перевірки

`autoload`

Чи потрібно [автоматично підвантажувати](language.oop5.autoload.md) клас, якщо він ще не завантажений.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо трейт існує, в іншому випадку повертає **`false`**
