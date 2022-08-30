Склеює всі значення в рядок

-   [« DsVector::isEmpty](ds-vector.isempty.html)
    
-   [ДсVector::jsonSerialize »](ds-vector.jsonserialize.html)
    
-   [PHP Manual](index.html)
    
-   [Вектор](class.ds-vector.html)
    
-   Склеює всі значення в рядок
    

# ДсVector::join

(PECL ds >= 1.0.0)

ДсVector::join — Склеює всі значення в рядок

### Опис

```methodsynopsis
public Ds\Vector::join(string $glue = ?): string
```

Склеює всі значення в рядок, опціонально використовуючи заданий роздільник.

### Список параметрів

`glue`

Необов'язковий параметр, який визначає роздільник між значеннями.

### Значення, що повертаються

Всі значення вектора склеєні в один рядок.

### Приклади

**Приклад #1 Приклад використання **ДсVector::join()** з роздільником**

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join("|"));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "a|b|c|1|2|3"
```

**Приклад #2 Приклад використання **ДсVector::join()** без роздільника**

```php
<?php
$vector = new \Ds\Vector(["a", "b", "c", 1, 2, 3]);

var_dump($vector->join());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(11) "abc123"
```