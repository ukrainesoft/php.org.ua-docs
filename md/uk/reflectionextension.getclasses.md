---
navigation:
  - reflectionextension.export.md: '« ReflectionExtension::export'
  - reflectionextension.getclassnames.md: 'ReflectionExtension::getClassNames »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getClasses'
---
# ReflectionExtension::getClasses

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getClasses — Повертає класи

### Опис

```methodsynopsis
public ReflectionExtension::getClasses(): array
```

Повертає перелік класів модуля.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив об'єктів класу [ReflectionClass](class.reflectionclass.md)по одному на кожен клас модуля. Якщо не визначено жодного класу, повертається порожній масив.

### Приклади

**Приклад #1 Приклад використання **ReflectionExtension::getClasses()****

```php
<?php
$ext = new ReflectionExtension('XMLWriter');
var_dump($ext->getClasses());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
array(1) {
  ["XMLWriter"]=>
  object(ReflectionClass)#2 (1) {
    ["name"]=>
    string(9) "XMLWriter"
  }
}
```

### Дивіться також

-   [ReflectionExtension::getClassNames()](reflectionextension.getclassnames.md) - Отримання імен класів
