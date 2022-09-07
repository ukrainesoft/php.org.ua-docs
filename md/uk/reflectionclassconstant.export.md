---
navigation:
  - reflectionclassconstant.construct.md: '« ReflectionClassConstant::construct'
  - reflectionclassconstant.getattributes.md: 'ReflectionClassConstant::getAttributes »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::export'
---
# ReflectionClassConstant::export

(PHP 7> = 7.1.0)

ReflectionClassConstant::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionClassConstant::export(mixed $class, string $name, bool $return = ?): string
```

Експортує reflection.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`class`

Експортований об'єкт Reflection.

`name`

Назва константи класу.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

### Дивіться також

-   [ReflectionClassConstant::toString()](reflectionclassconstant.tostring.md) - Повертає рядкове представлення об'єкта ReflectionClassConstant
