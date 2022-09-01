---
navigation:
  - reflectionextension.construct.md: '« ReflectionExtension::construct'
  - reflectionextension.getclasses.md: 'ReflectionExtension::getClasses »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::export'
---
# ReflectionExtension::export

(PHP 5, PHP 7)

ReflectionExtension::export — Експортує модуль

**Увага**

Ця функція *ЗАСТАРІЛА*, починаючи з PHP 7.4.0 і була *ВИДАЛЕНО*починаючи з PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionExtension::export(string $name, string $return = false): string
```

Експортує відбитий модуль. Формат виведення цієї функції такий самий як і при CLI-параметрі `--re [extension]`

### Список параметрів

`name`

Експортований об'єкт Reflection.

`return`

Встановлення в **`true`** поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return` встановлений в **`true`**, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionExtension::info()](reflectionextension.info.md) - Виведення інформації про модуль
-   [ReflectionExtension::toString()](reflectionextension.tostring.md) - Перетворення на рядок
