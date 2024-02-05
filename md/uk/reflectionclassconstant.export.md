---
navigation:
  - reflectionclassconstant.construct.md: '« ReflectionClassConstant::\_\_construct'
  - reflectionclassconstant.getattributes.md: 'ReflectionClassConstant::getAttributes »'
  - index.md: PHP Manual
  - class.reflectionclassconstant.md: ReflectionClassConstant
title: 'ReflectionClassConstant::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClassConstant::export

(PHP 7 >= 7.1.0)

ReflectionClassConstant::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionClassConstant::export(mixed $class, string $name, bool $return = ?): string
```

Експортує reflection.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`class`

Експортований об'єкт Reflection.

`name`

Ім'я константи класу.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

### Дивіться також

-   [ReflectionClassConstant::\_\_toString()](reflectionclassconstant.tostring.md) \- Повертає рядкове представлення об'єкта ReflectionClassConstant
