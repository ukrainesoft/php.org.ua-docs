Отримати ключ згенерованого елемента

-   [« Generator::getReturn](generator.getreturn.html)
    
-   [Generator::next »](generator.next.html)
    
-   [PHP Manual](index.html)
    
-   [Generator](class.generator.html)
    
-   Отримати ключ згенерованого елемента
    

# Generator::key

(PHP 5> = 5.5.0, PHP 7, PHP 8)

Generator::key — Отримати ключ згенерованого елемента

### Опис

```methodsynopsis
public Generator::key(): mixed
```

Отримує ключ згенерованого елемента.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ключ згенерованого елемента.

### Приклади

**Приклад #1 Приклад використання **Generator::key()****

```php
<?php

function Gen()
{
    yield 'key' => 'value';
}

$gen = Gen();

echo "{$gen->key()} => {$gen->current()}";
```

Результат виконання цього прикладу:

```
key => value
```