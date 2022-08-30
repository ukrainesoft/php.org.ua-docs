Вставляє значення за вказаним індексом

-   [« DsVector::get](ds-vector.get.html)
    
-   [ДсVector::isEmpty »](ds-vector.isempty.html)
    
-   [PHP Manual](index.md)
    
-   [Вектор](class.ds-vector.html)
    
-   Вставляє значення за вказаним індексом
    

# ДсVector::insert

(PECL ds >= 1.0.0)

ДсVector::insert — Вставляє значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Vector::insert(int $index, mixed ...$values): void
```

Вставляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, за яким необхідно здійснити вставку . `0 <= index <= count`

> **Зауваження**
> 
> Можна вказати індекс, що дорівнює кількості елементів вектора.

`values`

Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md) у разі некоректного індексу.

### Приклади

**Приклад #1 Приклад використання **ДсVector::insert()****

```php
<?php
$vector = new \Ds\Vector();

$vector->insert(0, "e");             // [e]
$vector->insert(1, "f");             // [e, f]
$vector->insert(2, "g");             // [e, f, g]
$vector->insert(0, "a", "b");        // [a, b, e, f, g]
$vector->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($vector);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Vector)#1 (7) {
  [0]=>
  string(1) "a"
  [1]=>
  string(1) "b"
  [2]=>
  string(1) "c"
  [3]=>
  string(1) "d"
  [4]=>
  string(1) "e"
  [5]=>
  string(1) "f"
  [6]=>
  string(1) "g"
}
```