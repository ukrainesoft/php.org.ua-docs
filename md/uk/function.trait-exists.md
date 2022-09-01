---
navigation:
  - function.property-exists.html: « propertyexists
  - book.ctype.html: Ctype »
  - index.html: PHP Manual
  - ref.classobj.html: Функції роботи з класами та об'єктами
title: traitexists
---
# traitexists

(PHP 5> = 5.4.0, PHP 7, PHP 8)

traitexists — Перевіряє, чи існує трейт

### Опис

```methodsynopsis
trait_exists(string $trait, bool $autoload = true): bool
```

### Список параметрів

`trait`

Ім'я трейту для перевірки

`autoload`

Чи намагатиметься його завантажити автоматично

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо трейт існує, в іншому випадку повертає **`false`**
