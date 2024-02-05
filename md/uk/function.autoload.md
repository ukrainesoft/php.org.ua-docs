---
navigation:
  - ref.classobj.md: « Функції роботи з класами та об'єктами
  - function.class-alias.md: class\_alias »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: \_\_autoload
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# \_\_autoload

(PHP 5, PHP 7)

\_\_autoload — Спроба завантажити невизначений клас

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
__autoload(string $class): void
```

Ви можете визначити цю функцію для [автозавантаження класів](language.oop5.autoload.md)

### Список параметрів

`class`

Ім'я класу, що завантажується

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [spl\_autoload\_register()](function.spl-autoload-register.md) \- Реєструє задану функцію як реалізацію методу\_\_autoload()
