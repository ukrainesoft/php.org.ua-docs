---
navigation:
  - function.iterator-to-array.md: « iteratorтоarray
  - function.spl-autoload-extensions.md: splautoloadextensions »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: splautoloadcall
---
# splautoloadcall

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadcall — Спроба завантажити клас усіма зареєстрованими функціями autoload()

### Опис

```methodsynopsis
spl_autoload_call(string $class): void
```

Цю функцію можна використовувати для ручного пошуку класу або інтерфейсу, використовуючи всі зареєстровані методи autoload.

### Список параметрів

`class`

Ім'я класу, що шукається.

### Значення, що повертаються

Функція не повертає значення після виконання.
