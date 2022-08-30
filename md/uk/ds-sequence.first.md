Повертає перший елемент колекції

-   [« DsSequence::find](ds-sequence.find.html)
    
-   [ДсSequence::get »](ds-sequence.get.html)
    
-   [PHP Manual](index.md)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Повертає перший елемент колекції
    

# ДсSequence::first

(PECL ds >= 1.0.0)

ДсSequence::first — Повертає перший елемент колекції

### Опис

```methodsynopsis
abstract public Ds\Sequence::first(): mixed
```

Повертає перший елемент колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент колекції.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.md)якщо колекція порожня.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::first()****

```php
<?php
$sequence = new \Ds\Vector([1, 2, 3]);
var_dump($sequence->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```