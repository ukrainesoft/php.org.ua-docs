---
navigation:
  - reflectionproperty.isdefault.md: '« ReflectionProperty::isDefault'
  - reflectionproperty.isprivate.md: 'ReflectionProperty::isPrivate »'
  - index.md: PHP Manual
  - class.reflectionproperty.md: ReflectionProperty
title: 'ReflectionProperty::isInitialized'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ReflectionProperty::isInitialized

(PHP 7 >= 7.4.0, PHP 8)

ReflectionProperty::isInitialized — Перевірити, чи ініціалізована властивість

### Опис

```methodsynopsis
public ReflectionProperty::isInitialized(?object $object = null): bool
```

Перевіряє, чи ініціалізована властивість.

### Список параметрів

`object`

Якщо властивість не статична, необхідно передати об'єкт, котрій буде проводитися перевірка.

### Значення, що повертаються

Повертає **`false`** для типизованих властивостей, яким не було надано значення і для властивостей, до яких явно застосували функцію [unset()](function.unset.md). Для решти властивостей повертає **`true`**

### Помилки

Кидає виняток [ReflectionException](class.reflectionexception.md) якщо властивість недоступна. Доступ до protected і private властивостей можна отримати за допомогою [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `object` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** ReflectionProperty::isInitialized()\*\*\*\*

```php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
$user = new User;
var_dump($rp->isInitialized($user));
$user->name = 'Nikita';
var_dump($rp->isInitialized($user));
?>
```

Результат виконання наведеного прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionProperty::hasType()](reflectionproperty.hastype.md) \- Перевірити, чи заданий для властивості тип
