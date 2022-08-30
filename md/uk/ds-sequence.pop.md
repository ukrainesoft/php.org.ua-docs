Видаляє та повертає останнє значення

-   [« DsSequence::merge](ds-sequence.merge.html)
    
-   [ДсSequence::push »](ds-sequence.push.html)
    
-   [PHP Manual](index.html)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Видаляє та повертає останнє значення
    

# ДсSequence::pop

(PECL ds >= 1.0.0)

ДсSequence::pop — Видаляє та повертає останнє значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::pop(): mixed
```

Видаляє та повертає останнє значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останнє віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::pop()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);

var_dump($sequence->pop());
var_dump($sequence->pop());
var_dump($sequence->pop());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
int(2)
int(1)
```