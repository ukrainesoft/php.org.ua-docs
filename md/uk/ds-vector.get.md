Повертає значення за індексом

-   [« DsVector::first](ds-vector.first.html)
    
-   [ДсVector::insert »](ds-vector.insert.html)
    
-   [PHP Manual](index.md)
    
-   [Вектор](class.ds-vector.html)
    
-   Повертає значення за індексом
    

# ДсVector::get

(PECL ds >= 1.0.0)

ДсVector::get — Повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Vector::get(int $index): mixed
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

**Приклад #1 Приклад використання **ДсVector::get()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector->get(0));
var_dump($vector->get(1));
var_dump($vector->get(2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Приклад #2 Приклад використання **ДсVector::get()** із синтаксисом масиву**

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

var_dump($vector[0]);
var_dump($vector[1]);
var_dump($vector[2]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```