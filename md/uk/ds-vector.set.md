Замінює значення за вказаним індексом

-   [« Ds\\Vector::rotate](ds-vector.rotate.html)
    
-   [Ds\\Vector::shift »](ds-vector.shift.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Замінює значення за вказаним індексом
    

# ДсVector::set

(PECL ds >= 1.0.0)

ДсVector::set — Замінює значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Vector::set(int $index, mixed $value): void
```

Замінює значення за вказаним індексом.

### Список параметрів

`index`

Індекс, яким треба замінити значення.

`value`

Нове значення.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсVector::set()****

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector->set(1, "_");
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```

**Приклад #2 Приклад використання **ДсVector::set()** із синтаксисом масиву**

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c"]);

$vector[1] = "_";
print_r($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Ds\Vector Object
(
    [0] => a
    [1] => _
    [2] => c
)
```