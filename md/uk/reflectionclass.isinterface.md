---
navigation:
  - reflectionclass.isinstantiable.md: '« ReflectionClass::isInstantiable'
  - reflectionclass.isinternal.md: 'ReflectionClass::isInternal »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isInterface'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isInterface

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isInterface — Перевіряє, чи клас є інтерфейсом

### Опис

```methodsynopsis
public ReflectionClass::isInterface(): bool
```

Перевіряє, чи є клас інтерфейсом чи ні.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ReflectionClass::isInterface()\*\*\*\*

```php
<?php
interface SomeInterface {
    public function interfaceMethod();
}

$class = new ReflectionClass('SomeInterface');
var_dump($class->isInterface());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionClass::isInstance()](reflectionclass.isinstance.md) \- Перевіряє, чи належить об'єкт класу
