---
navigation:
  - reflectionproperty.construct.md: '« ReflectionProperty::\_\_construct'
  - reflectionproperty.getattributes.md: 'ReflectionProperty::getAttributes »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::export

(PHP 5, PHP 7)

ReflectionProperty::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionProperty::export(mixed $class, string $name, bool $return = ?): string
```

Експортує відображення (reflection).

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`name`

Ім'я якості.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

### Дивіться також

-   [ReflectionProperty::\_\_toString()](reflectionproperty.tostring.md) \- Перетворення на рядок
