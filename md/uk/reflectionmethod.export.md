---
navigation:
  - reflectionmethod.createfrommethodname.md: '« ReflectionMethod::createFromMethodName'
  - reflectionmethod.getclosure.md: 'ReflectionMethod::getClosure »'
  - index.md: PHP Manual
  - class.reflectionmethod.md: ReflectionMethod
title: 'ReflectionMethod::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionMethod::export

(PHP 5, PHP 7)

ReflectionMethod::export — Експорт відбитого методу

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionMethod::export(string $class, string $name, bool $return = false): string
```

Експортує ReflectionMethod.

### Список параметрів

`class`

Назва класу.

`name`

Ім'я методу.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return`установлен в\*\*`true`\*\*, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionMethod::\_\_construct()](reflectionmethod.construct.md) \- Конструктор класу ReflectionMethod
-   [ReflectionMethod::\_\_toString()](reflectionmethod.tostring.md) \- Повертає рядкову виставу об'єкта ReflectionMethod
