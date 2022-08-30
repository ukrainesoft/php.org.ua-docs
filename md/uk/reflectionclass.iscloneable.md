Перевіряє, чи можна клонувати цей клас

-   [« ReflectionClass::isAnonymous](reflectionclass.isanonymous.md)
    
-   [ReflectionClass::isEnum »](reflectionclass.isenum.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionClass](class.reflectionclass.md)
    
-   Перевіряє, чи можна клонувати цей клас
    

# ReflectionClass::isCloneable

(PHP 5> = 5.4.0, PHP 7, PHP 8)

ReflectionClass::isCloneable — Перевіряє, чи можна клонувати цей клас

### Опис

```methodsynopsis
public ReflectionClass::isCloneable(): bool
```

Перевіряє, чи можна клонувати цей клас.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо клас можна клонувати, в іншому випадку **`false`**

### Приклади

**Приклад #1 Приклад використання **ReflectionClass::isCloneable()****

```php
<?php
class NotCloneable {
    public $var1;

    private function __clone() {
    }
}

class Cloneable {
    public $var1;
}

$notCloneable = new ReflectionClass('NotCloneable');
$cloneable = new ReflectionClass('Cloneable');

var_dump($notCloneable->isCloneable());
var_dump($cloneable->isCloneable());
?>
```

Результат виконання цього прикладу:

```
bool(false)
bool(true)
```