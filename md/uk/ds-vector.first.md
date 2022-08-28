Повертає перший елемент вектора

-   [« Ds\\Vector::find](ds-vector.find.html)
    
-   [Ds\\Vector::get »](ds-vector.get.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Повертає перший елемент вектора
    

# ДсVector::first

(PECL ds >= 1.0.0)

ДсVector::first — Повертає перший елемент вектора

### Опис

```methodsynopsis
public Ds\Vector::first(): mixed
```

Повертає перший елемент вектор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Перший елемент вектор.

### Помилки

Викидає виняток [UnderflowException](class.underflowexception.html)якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **ДсVector::first()****

```php
<?php
$vector = new \Ds\Vector([1, 2, 3]);
var_dump($vector->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1)
```