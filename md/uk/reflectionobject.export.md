---
navigation:
  - reflectionobject.construct.md: '« ReflectionObject::\_\_construct'
  - class.reflectionparameter.md: ReflectionParameter »
  - index.md: PHP Manual
  - class.reflectionobject.md: ReflectionObject
title: 'ReflectionObject::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionObject::export

(PHP 5, PHP 7)

ReflectionObject::export — Експорт

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionObject::export(string $argument, bool $return = ?): string
```

Експортує відображення (reflection).

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`argument`

Експортований об'єкт Reflection.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return`установлен в\*\*`true`\*\*, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionObject::\_\_construct()](reflectionobject.construct.md) \- Конструктор класу ReflectionObject
