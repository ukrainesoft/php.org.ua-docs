Повертає значення за індексом

-   [« Ds\\Deque::first](ds-deque.first.html)
    
-   [Ds\\Deque::insert »](ds-deque.insert.html)
    
-   [PHP Manual](index.html)
    
-   [Двухсторонняя очередь](class.ds-deque.html)
    
-   Повертає значення за індексом
    

# ДсDeque::get

(PECL ds >= 1.0.0)

ДсDeque::get — Повертає значення за індексом

### Опис

```methodsynopsis
public Ds\Deque::get(int $index): mixed
```

Повертає значення за заданим індексом.

### Список параметрів

`index`

Індекс. Перший елемент має індекс 0.

### Значення, що повертаються

Значення за заданим індексом.

### Помилки

Викидає виняток [OutOfRangeException](class.outofrangeexception.html)якщо індекс некоректний.

### Приклади

**Приклад #1 Приклад використання **ДсDeque::get()****

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque->get(0));
var_dump($deque->get(1));
var_dump($deque->get(2));
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```

**Приклад #2 Приклад використання **ДсDeque::get()** із синтаксисом масиву**

```php
<?php
$deque = new \Ds\Deque(["a", "b", "c"]);

var_dump($deque[0]);
var_dump($deque[1]);
var_dump($deque[2]);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(1) "a"
string(1) "b"
string(1) "c"
```