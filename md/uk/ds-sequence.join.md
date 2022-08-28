Склеює всі значення в рядок

-   [« Ds\\Sequence::insert](ds-sequence.insert.html)
    
-   [Ds\\Sequence::last »](ds-sequence.last.html)
    
-   [PHP Manual](index.html)
    
-   [Последовательность](class.ds-sequence.html)
    
-   Склеює всі значення в рядок
    

# ДсSequence::join

(PECL ds >= 1.0.0)

ДсSequence::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
abstract public Ds\Sequence::join(string $glue = ?): string
```

Склеює всі значення у рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Усі значення колекції склеєні в один рядок.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::join()** з роздільником**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join("|"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "a|b|c|1|2|3"
```

**Приклад #2 Приклад використання **ДсSequence::join()** без роздільника**

```php
<?php
$sequence = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($sequence->join());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "abc123"
```