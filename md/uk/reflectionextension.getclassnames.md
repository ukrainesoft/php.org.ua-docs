---
navigation:
  - reflectionextension.getclasses.md: '« ReflectionExtension::getClasses'
  - reflectionextension.getconstants.md: 'ReflectionExtension::getConstants »'
  - index.md: PHP Manual
  - class.reflectionextension.md: ReflectionExtension
title: 'ReflectionExtension::getClassNames'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionExtension::getClassNames

(PHP 5, PHP 7, PHP 8)

ReflectionExtension::getClassNames — Отримання імен класів

### Опис

```methodsynopsis
public ReflectionExtension::getClassNames(): array
```

Отримує список імен класів, як визначено в модулі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив (array) імен класів, визначених у модулі. Якщо жодних класів не визначено, буде повернено порожній масив.

### Приклади

**Приклад #1 Приклад використання** ReflectionExtension::getClassNames()\*\*\*\*

```php
<?php
$ext = new ReflectionExtension('XMLWriter');
var_dump($ext->getClassNames());
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(1) {
  [0]=>
  string(9) "XMLWriter"
}
```

### Дивіться також

-   [ReflectionExtension::getClasses()](reflectionextension.getclasses.md) \- Повертає класи
-   [ReflectionExtension::getName()](reflectionextension.getname.md) \- Отримання імені модуля
