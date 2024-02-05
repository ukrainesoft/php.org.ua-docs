---
navigation:
  - reflectionclass.getextension.md: '« ReflectionClass::getExtension'
  - reflectionclass.getfilename.md: 'ReflectionClass::getFileName »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getExtensionName'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getExtensionName

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getExtensionName — Повертає ім'я модуля, що визначає клас

### Опис

```methodsynopsis
public ReflectionClass::getExtensionName(): string|false
```

Повертає ім'я модуля, який визначає клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Имя модуля, определяющее класс, или\*\*`false`\*\* для класів користувача.

### Приклади

**Пример #1 Пример использования**ReflectionClass::getExtensionName()\*\*\*\*

```php
<?php
$class = new ReflectionClass('ReflectionClass');
$extension = $class->getExtensionName();
var_dump($extension);
?>
```

Результат виконання наведеного прикладу:

```
string(10) "Reflection"
```

### Дивіться також

-   [ReflectionClass::getExtension()](reflectionclass.getextension.md) \- Повертає об'єкт класу ReflectionExtension для модуля, що визначає клас
