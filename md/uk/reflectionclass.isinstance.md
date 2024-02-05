---
navigation:
  - reflectionclass.isfinal.md: '« ReflectionClass::isFinal'
  - reflectionclass.isinstantiable.md: 'ReflectionClass::isInstantiable »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isInstance'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionClass::isInstance

(PHP 5, PHP 7, PHP 8)

ReflectionClass::isInstance — Перевіряє, чи належить об'єкт класу

### Опис

```methodsynopsis
public ReflectionClass::isInstance(object $object): bool
```

Перевіряє, чи є об'єкт екземпляром класу.

### Список параметрів

`object`

Об'єкт, що перевіряється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ReflectionClass::isInstance()\*\* та його аналогів\*\*

```php
<?php
// Пример использования
$class = new ReflectionClass('Foo');

if ($class->isInstance($arg)) {
    echo "Yes";
}

// Аналогично этому
if ($arg instanceof Foo) {
    echo "Yes";
}

// Аналогично этому
if (is_a($arg, 'Foo')) {
    echo "Yes";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Yes
Yes
Yes
```

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) \- Перевіряє, чи є клас інтерфейсом
-   [Оператори перевірки типу (instanceof)](language.operators.type.md)
-   [Інтерфейси об'єктів](language.oop5.interfaces.md)
-   [is\_a()](function.is-a.md) \- Перевіряє, чи об'єкт належить до типу або підтипу
