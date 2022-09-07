---
navigation:
  - class.reflection.md: « Reflection
  - reflection.getmodifiernames.md: 'Reflection::getModifierNames »'
  - index.md: PHP Manual
  - class.reflection.md: Reflection
title: 'Reflection::export'
---
# Reflection::export

(PHP 5, PHP 7)

Reflection::export — Експортує Reflection

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static Reflection::export(Reflector $reflector, bool $return = false): string
```

Експортує reflection.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`reflector`

Експортований об'єкт Reflection.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [Reflection::getModifierNames()](reflection.getmodifiernames.md) - Отримання імен модифікаторів
