---
navigation:
  - reflectionclass.getdoccomment.md: '« ReflectionClass::getDocComment'
  - reflectionclass.getextension.md: 'ReflectionClass::getExtension »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::getEndLine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::getEndLine

(PHP 5, PHP 7, PHP 8)

ReflectionClass::getEndLine — Повертає номер останнього рядка

### Опис

```methodsynopsis
public ReflectionClass::getEndLine(): int|false
```

Повертає номер останнього рядка з визначення класу користувача.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Номер останнього рядка з визначення класу користувача або **`false`**, якщо номер невідомий.

### Приклади

**Приклад #1 Приклад використання** ReflectionClass::getEndLine()\*\*\*\*

```php
<?php
// Тестовый класс
class TestClass { }

$rc = new ReflectionClass('TestClass');

echo $rc->getEndLine();
?>
```

Результат виконання наведеного прикладу:

```
3
```

### Дивіться також

-   [ReflectionClass::getStartLine()](reflectionclass.getstartline.md) \- Повертає номер початкового рядка
