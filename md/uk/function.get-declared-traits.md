---
navigation:
  - function.get-declared-interfaces.html: « getdeclaredinterfaces
  - function.get-mangled-object-vars.html: getmangledobjectvars »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getdeclaredtraits
---
# getdeclaredtraits

(PHP 5> = 5.4.0, PHP 7, PHP 8)

getdeclaredtraits — Повертає масив з усіма оголошеними трейтами

### Опис

```methodsynopsis
get_declared_traits(): array
```

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з іменами трейтів як значення масиву. Повертає \*\*`null`\*\*якщо такі не знайдені.

### Дивіться також

-   [classuses()](function.class-uses.md) - Повертає список трейтів, які використовуються заданим класом
-   [traitexists()](function.trait-exists.md) - Перевіряє, чи існує трейт
