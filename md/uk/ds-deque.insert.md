Вставляє значення за вказаним індексом

-   [« Ds\\Deque::get](ds-deque.get.html)
    
-   [Ds\\Deque::isEmpty »](ds-deque.isempty.html)
    
-   [PHP Manual](index.html)
    
-   [Двухсторонняя очередь](class.ds-deque.html)
    
-   Вставляє значення за вказаним індексом
    

# ДсDeque::insert

(PECL ds >= 1.0.0)

ДсDeque::insert — Вставляє значення за вказаним індексом

### Опис

```methodsynopsis
public Ds\Deque::insert(int $index, mixed ...$values): void
```

Вставляє значення за вказаним індексом.

### Список параметрів

`index`

Індекс, за яким необхідно здійснити вставку . `0 <= index <= count`

> **Зауваження**
> 
> Можна вказувати індекс, що дорівнює кількості елементів двосторонньої черги.

`values`

Значення чи значення для вставки.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html) у разі некоректного індексу.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::insert()****

```php
<?php
$deque = new \Ds\Deque();

$deque->insert(0, "e");             // [e]
$deque->insert(1, "f");             // [e, f]
$deque->insert(2, "g");             // [e, f, g]
$deque->insert(0, "a", "b");        // [a, b, e, f, g]
$deque->insert(2, ...["c", "d"]);   // [a, b, c, d, e, f, g]

var_dump($deque);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
object(Ds\Deque)#1 (7) {
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