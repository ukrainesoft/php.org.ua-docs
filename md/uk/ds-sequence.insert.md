Вставляє значення за вказаним індексом

-   [« DsSequence::get](ds-sequence.get.html)
    
-   [ДсSequence::join »](ds-sequence.join.html)
    
-   [PHP Manual](index.html)
    
-   [Послідовність](class.ds-sequence.html)
    
-   Вставляє значення за вказаним індексом
    

# ДсSequence::insert

(PECL ds >= 1.0.0)

ДсSequence::insert — Вставляє значення за вказаним індексом

### Опис

```methodsynopsis
abstract public Ds\Sequence::insert(int $index, mixed ...$values): void
```

Вставляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, за яким необхідно здійснити вставку . `0 <= index <= count`

> **Зауваження**
> 
> Можна вказати індекс, який дорівнює кількості елементів колекції.

`values`

Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html) у разі некоректного індексу.

### Приклади

**Приклад #1 Приклад використання **ДсSequence::insert()****

```php
<?php
$sequence = new \Ds\Vector();

$sequence->insert(0, "e");             // [e]
$sequence->insert(1, "f");             // [e, f]
$sequence->insert(2, "g");             // [e, f, g]
$sequence->insert(0, "a", "b");        // [a, b, e, f, g]
$sequence->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($sequence);
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