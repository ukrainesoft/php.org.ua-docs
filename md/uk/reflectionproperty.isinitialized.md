---
navigation:
  - reflectionproperty.isdefault.html: '« ReflectionProperty::isDefault'
  - reflectionproperty.isprivate.html: 'ReflectionProperty::isPrivate »'
  - index.html: PHP Manual
  - class.reflectionproperty.html: ReflectionProperty
title: 'ReflectionProperty::isInitialized'
---
# ReflectionProperty::isInitialized

(PHP 7> = 7.4.0, PHP 8)

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

Повертає **`false`** для типизованих властивостей, яким не було надано значення і для властивостей, до яких явно застосували функцію [unset()](function.unset.html). Для решти властивостей повертає **`true`**

### Помилки

Кидає виняток [ReflectionException](class.reflectionexception.html) якщо властивість недоступна. Доступ до protected і private властивостей можна отримати за допомогою [ReflectionProperty::setAccessible()](reflectionproperty.setaccessible.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | `object` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **ReflectionProperty::isInitialized()****

```php
<?php
class User
{
    public string $name;
}

$rp = new ReflectionProperty('User', 'name');
$user = new User;
var_dump($rp->isInitialized($user));
$user->name = 'Nikita';
var_dump($rp->isInitialized($user));
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```

### Дивіться також

-   [ReflectionProperty::hasType()](reflectionproperty.hastype.html) - Перевірити, чи заданий для властивості тип
