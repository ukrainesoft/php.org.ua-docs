---
navigation:
  - reflectionfunction.construct.md: '« ReflectionFunction::\_\_construct'
  - reflectionfunction.getclosure.md: 'ReflectionFunction::getClosure »'
  - index.md: PHP Manual
  - class.reflectionfunction.md: ReflectionFunction
title: 'ReflectionFunction::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionFunction::export

(PHP 5, PHP 7)

ReflectionFunction::export — Експортує функції

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionFunction::export(string $name, string $return = ?): string
```

Експортує відображену (reflected) функцію.

### Список параметрів

`name`

Експортований об'єкт Reflection.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return`установлен в\*\*`true`\*\*, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionFunction::invoke()](reflectionfunction.invoke.md) \- Викликає функцію
-   [ReflectionFunction::\_\_toString()](reflectionfunction.tostring.md) \- Повертає рядкову виставу об'єкта ReflectionFunction
