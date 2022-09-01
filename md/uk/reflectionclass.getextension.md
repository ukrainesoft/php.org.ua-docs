---
navigation:
  - reflectionclass.getendline.html: '« ReflectionClass::getEndLine'
  - reflectionclass.getextensionname.html: 'ReflectionClass::getExtensionName »'
  - index.html: PHP Manual
  - class.reflectionclass.html: ReflectionClass
title: 'ReflectionClass::getExtension'
---
# ReflectionClass::getExtension

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getExtension — Повертає об'єкт класу [ReflectionExtension](class.reflectionextension.html) для модуля, що визначає клас

### Опис

```methodsynopsis
public ReflectionClass::getExtension(): ?ReflectionExtension
```

Повертає об'єкт класу [ReflectionExtension](class.reflectionextension.html) для модуля, що визначає клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр класу [ReflectionExtension](class.reflectionextension.html), Що представляє модуль, що визначає клас, або **`null`** для класів користувача.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::getExtension()****

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtension();
var_dump($extension);
?>
```

Результат виконання цього прикладу:

```
object(ReflectionExtension)#2 (1) {
  ["name"]=>
  string(10) "Reflection"
}
```

### Дивіться також

-   [ReflectionClass::getExtensionName()](reflectionclass.getextensionname.html) - Повертає ім'я модуля, що визначає клас
