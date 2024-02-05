---
navigation:
  - ds-sequence.get.md: '« Ds\\Sequence::get'
  - ds-sequence.join.md: 'Ds\\Sequence::join »'
  - index.md: PHP Manual
  - class.ds-sequence.md: Ds\\Sequence
title: 'Ds\\Sequence::insert'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Sequence::insert

(PECL ds >= 1.0.0)

Ds\\Sequence::insert — Вставляє значення за вказаним індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::insert(int $index, mixed ...$values): void
```

Вставляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, за яким необхідно здійснити вставку . `0 <= index <= count`

> **Зауваження** :
> 
> Можна вказати індекс, який дорівнює кількості елементів колекції.

`values`

Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.md) у разі некоректного індексу.

### Приклади

**Приклад #1 Приклад використання** Ds\\Sequence::insert()\*\*\*\*

```php
<?php
$sequence = new \Ds\Vector();

$sequence->insert(0, "e");             // [e]
$sequence->insert(1, "f");             // [e, f]
$sequence->insert(2, "g");             // [e, f, g]
$sequence->insert(0, "a", "b");        // [a, b, e, f, g]
$sequence->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($sequence);
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
