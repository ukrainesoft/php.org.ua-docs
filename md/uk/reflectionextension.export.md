---
navigation:
  - reflectionextension.construct.md: '« ReflectionExtension::\_\_construct'
  - reflectionextension.getclasses.md: 'ReflectionExtension::getClasses »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::export'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::export

(PHP 5, PHP 7)

ReflectionExtension::export — Експортує модуль

**Увага**

Ця функція *ЗАСТАРІЛА* починаючи з PHP 7.4.0 і була *ВИДАЛЕНО* у PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
public static ReflectionExtension::export(string $name, string $return = false): string
```

Експортує відбитий модуль. Формат виведення цієї функції такий самий, як і при CLI-параметрі `--re [extension]`

### Список параметрів

`name`

Експортований об'єкт Reflection.

`return`

Установка в\*\*`true`\*\* поверне експортоване значення, на відміну поведінки, де цей параметр опущений. Встановлення в **`false`** (за умовчанням) зробить протилежне.

### Значення, що повертаються

Якщо параметр `return`установлен в\*\*`true`\*\*, тоді експортований об'єкт буде повернутий як string, інакше буде повернутий **`null`**

### Дивіться також

-   [ReflectionExtension::info()](reflectionextension.info.md) \- Виведення інформації про модуль
-   [ReflectionExtension::\_\_toString()](reflectionextension.tostring.md) \- Перетворення на рядок
