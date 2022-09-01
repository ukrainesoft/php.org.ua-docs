---
navigation:
  - ref.classobj.md: « Функції роботи з класами та об'єктами
  - function.class-alias.html: classalias »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: autoload
---
# autoload

(PHP 5, PHP 7)

autoload — Спроба завантажити невизначений клас

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.2.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
__autoload(string $class): void
```

Ви можете визначити цю функцію для [автозагрузки классов](language.oop5.autoload.md)

### Список параметрів

`class`

Ім'я класу, що завантажується

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [splautoloadregister()](function.spl-autoload-register.md) - Реєструє задану функцію як реалізацію методу autoload()
