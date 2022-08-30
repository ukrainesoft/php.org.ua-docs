Повертає значення за індексом

-   [« DsSet::first](ds-set.first.html)
    
-   [ДсSet::intersect »](ds-set.intersect.html)
    
-   [PHP Manual](index.md)
    
-   [Набор](class.ds-set.html)
    
-   Повертає значення за індексом
    

# ДсSet::get

(PECL ds >= 1.0.0)

ДсSet::get — Повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Set::get(int $index): mixed
```

Повертає значення за заданим індексом.

### Список параметрів

`index`

Індекс. Перший елемент має індекс 0.

### Значення, що повертаються

Значення за заданим індексом.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсSet::get()****

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set->get(0));
var_dump($set->get(1));
var_dump($set->get(2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Приклад #2 Приклад використання **ДсSet::get()** із синтаксисом масиву**

```php
<?php
$set = new \Ds\Set(["a", "b", "c"]);

var_dump($set[0]);
var_dump($set[1]);
var_dump($set[2]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```