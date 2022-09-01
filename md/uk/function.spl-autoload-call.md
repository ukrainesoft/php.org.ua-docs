---
navigation:
  - function.iterator-to-array.html: « iteratorтоarray
  - function.spl-autoload-extensions.html: splautoloadextensions »
  - index.html: PHP Manual
  - ref.spl.html: Функції SPL
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
