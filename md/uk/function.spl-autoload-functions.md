---
navigation:
  - function.spl-autoload-extensions.md: « spl\_autoload\_extensions
  - function.spl-autoload-register.md: spl\_autoload\_register »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload\_functions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload\_functions

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload\_functions — отримання списку всіх зареєстрованих функцій \_\_autoload()

### Опис

```methodsynopsis
spl_autoload_functions(): array
```

Отримує список усіх зареєстрованих функцій \_\_autoload().

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) всіх зареєстрованих у \_\_autoload функцій. Якщо функція не зареєстрована або черга автозавантаження не активована, то значенням, що повертається, буде порожній масив.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Значення, що повертається, було оновлено і тепер завжди є масивом (array); раніше функція повертала **`false`**, якщо черга автозавантаження не була активована. |
