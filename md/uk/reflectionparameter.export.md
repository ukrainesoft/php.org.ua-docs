---
navigation:
  - reflectionparameter.construct.md: '« ReflectionParameter::construct'
  - reflectionparameter.getattributes.md: 'ReflectionParameter::getAttributes »'
  - index.md: PHP Manual
  - class.reflectionparameter.md: ReflectionParameter
title: 'ReflectionParameter::export'
---
# ReflectionParameter::export

(PHP 5, PHP 7)

ReflectionParameter::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionParameter::export(string $function, string $parameter, bool $return = ?): string
```

Експорт.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`function`

Ім'я функції.

`parameter`

Ім'я аргументу.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Експорт відбиття (reflection).

### Дивіться також

-   [ReflectionParameter::toString()](reflectionparameter.tostring.md) - Перетворення на рядок
