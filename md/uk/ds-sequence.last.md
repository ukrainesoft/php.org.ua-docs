Повертає останнє значення колекції

-   [« Ds\\Sequence::join](ds-sequence.join.html)
    
-   [Ds\\Sequence::map »](ds-sequence.map.html)
    
-   [PHP Manual](index.html)
    
-   [Последовательность](class.ds-sequence.html)
    
-   Повертає останнє значення колекції
    

# ДсSequence::last

(PECL ds >= 1.0.0)

ДсSequence::last — Повертає останнє значення колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::last(): mixed
```

Повертає останнє значення колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::last()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->last());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(3)
```