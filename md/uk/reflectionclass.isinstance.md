---
navigation:
  - reflectionclass.isfinal.md: '« ReflectionClass::isFinal'
  - reflectionclass.isinstantiable.md: 'ReflectionClass::isInstantiable »'
  - index.md: PHP Manual
  - class.reflectionclass.md: ReflectionClass
title: 'ReflectionClass::isInstance'
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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isInstance()** та його аналогів**

```php
<?php
// Пример использования
$class = new ReflectionClass('Foo');

if ($class->isInstance($arg)) {
    echo "Yes";
}

// Аналогично этому
if ($arg instanceof Foo) {
    echo "Yes";
}

// Аналогично этому
if (is_a($arg, 'Foo')) {
    echo "Yes";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Yes
Yes
Yes
```

### Дивіться також

-   [ReflectionClass::isInterface()](reflectionclass.isinterface.md) - Перевіряє, чи є клас інтерфейсом
-   [Оператори перевірки типу (instanceof)](language.operators.type.md)
-   [Інтерфейси об'єктів](language.oop5.interfaces.md)
-   [ісa()](function.is-a.html) - Перевіряє, чи належить об'єкт до цього класу чи чи є цей клас одним із його батьків
