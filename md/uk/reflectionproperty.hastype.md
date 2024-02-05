---
navigation:
  - reflectionproperty.hasdefaultvalue.md: '« ReflectionProperty::hasDefaultValue'
  - reflectionproperty.isdefault.md: 'ReflectionProperty::isDefault »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::hasType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::hasType

(PHP 7 >= 7.4.0, PHP 8)

ReflectionProperty::hasType — Перевірити, чи заданий для властивості тип

### Опис

```methodsynopsis
public ReflectionProperty::hasType(): bool
```

Перевірити, чи заданий для властивості тип.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Якщо тип заданий, то **`true`**, а якщо ні, то **`false`**

### Приклади

**Пример #1 Пример использования**ReflectionProperty::hasType()\*\*\*\*

```php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
var_dump($rp->hasType());
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
```

### Дивіться також

-   [ReflectionProperty::getType()](reflectionproperty.gettype.md) \- Отримати тип якості
-   [ReflectionProperty::isInitialized()](reflectionproperty.isinitialized.md) \- Перевірити, чи ініціалізована властивість
