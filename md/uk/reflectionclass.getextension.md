---
navigation:
  - reflectionclass.getendline.md: '« ReflectionClass::getEndLine'
  - reflectionclass.getextensionname.md: 'ReflectionClass::getExtensionName »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getExtension'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getExtension

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getExtension — Повертає об'єкт класу [ReflectionExtension](class.reflectionextension.md)для модуля, определяющего класс

### Опис

```methodsynopsis
public ReflectionClass::getExtension(): ?ReflectionExtension
```

Повертає об'єкт класу [ReflectionExtension](class.reflectionextension.md) для модуля, що визначає клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Екземпляр класу [ReflectionExtension](class.reflectionextension.md), представляющий модуль, определяющий класс, или\*\*`null`\*\* для класів користувача.

### Приклади

**Пример #1 Пример использования**ReflectionClass::getExtension()\*\*\*\*

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtension();
var_dump($extension);
?>
```

Результат виконання наведеного прикладу:

```
object(ReflectionExtension)#2 (1) {
  ["name"]=>
  string(10) "Reflection"
}
```

### Дивіться також

-   [ReflectionClass::getExtensionName()](reflectionclass.getextensionname.md) \- Повертає ім'я модуля, що визначає клас
