---
navigation:
  - ds-vector.get.md: '« Ds\\Vector::get'
  - ds-vector.isempty.md: 'Ds\\Vector::isEmpty »'
  - index.md: PHP Manual
  - class.ds-vector.md: Ds\\Vector
title: 'Ds\\Vector::insert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Vector::insert

(PECL ds >= 1.0.0)

Ds\\Vector::insert — Вставляє значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Vector::insert(int $index, mixed ...$values): void
```

Вставляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, за яким необхідно здійснити вставку . `0 <= index <= count`

> **Зауваження** :
> 
> Можна вказати індекс, що дорівнює кількості елементів вектора.

`values`

Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md) у разі некоректного індексу.

### Приклади

**Приклад #1 Приклад використання** Ds\\Vector::insert()\*\*\*\*

```php
<?php
$vector = new \Ds\Vector();

$vector->insert(0, "e");             // [e]
$vector->insert(1, "f");             // [e, f]
$vector->insert(2, "g");             // [e, f, g]
$vector->insert(0, "a", "b");        // [a, b, e, f, g]
$vector->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($vector);
?>
```

Висновок наведеного прикладу буде схожим на:

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
