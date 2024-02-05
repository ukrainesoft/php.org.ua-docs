---
navigation:
  - function.iterator-to-array.md: « iterator\_to\_array
  - function.spl-autoload-extensions.md: spl\_autoload\_extensions »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload\_call
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload\_call

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload\_call — Спроба завантажити клас усіма зареєстрованими функціями \_\_autoload()

### Опис

```methodsynopsis
spl_autoload_call(string $class): void
```

Цю функцію можна використовувати для ручного пошуку класу або інтерфейсу, використовуючи всі зареєстровані методи \_\_autoload.

### Список параметрів

`class`

Ім'я класу, що шукається.

### Значення, що повертаються

Функція не повертає значення після виконання.
