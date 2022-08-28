Видаляє та повертає перше значення

-   [« Ds\\Sequence::set](ds-sequence.set.html)
    
-   [Ds\\Sequence::slice »](ds-sequence.slice.html)
    
-   [PHP Manual](index.html)
    
-   [Последовательность](class.ds-sequence.html)
    
-   Видаляє та повертає перше значення
    

# ДсSequence::shift

(PECL ds >= 1.0.0)

ДсSequence::shift — Видаляє та повертає перше значення

### Опис

```methodsynopsis
abstract public Ds\Sequence::shift(): mixed
```

Видаляє та повертає перше значення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перше віддалене значення.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::shift()****

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c"]);

var_dump($sequence->shift());
var_dump($sequence->shift());
var_dump($sequence->shift());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```