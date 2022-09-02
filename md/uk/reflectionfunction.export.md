---
navigation:
  - reflectionfunction.construct.md: '« ReflectionFunction::construct'
  - reflectionfunction.getclosure.md: 'ReflectionFunction::getClosure »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::export'
---
# ReflectionFunction::export

(PHP 5, PHP 7)

ReflectionFunction::export — Експортує функції

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionFunction::export(string $name, string $return = ?): string
```

Експортує відображену (reflected) функцію.

### Список параметрів

`name`

Експортований об'єкт Reflection.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionFunction::invoke()](reflectionfunction.invoke.md) - Викликає функцію
-   [ReflectionFunction::toString()](reflectionfunction.tostring.md) - Подання у вигляді рядка
